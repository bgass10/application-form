<script>
  import { initializeApp } from "firebase/app";
  import { getFirestore, collection, getDocs } from "firebase/firestore/lite";

  const firebaseConfig = {
    apiKey: "AIzaSyCr-n--LHaeUX0B6ChWsmr0C0GiWVoO0c0",
    authDomain: "application-form-95707.firebaseapp.com",
    projectId: "application-form-95707",
    storageBucket: "application-form-95707.appspot.com",
    messagingSenderId: "304488650951",
    appId: "1:304488650951:web:f317d039e06b95f123c6e2",
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();

  const add = () => {
    db.collection("applications")
      .add({
        img: { src },
        name: { name },
        age: { age },
        city: { city },
        state: { state },
        hobbies: { hobbies },
        college: { college },
        major: { major },
        employment: { employment },
        feet: { feet },
        inches: { inches },
        religion: { religion },
        drinkVal: { drinkVal },
        smokeVal: { smokeVal },
        number: { number },
        instagram: { instagram },
        snapchat: { snapchat },
        artists: { artists },
        songs: { songs },
      })
      .then((docRef) => {
        console.log("Document written with ID: ", docRef.id);
      })
      .catch((error) => {
        console.error("Error adding document: ", error);
      });
  };

  import Heading from "./Heading.svelte";
  import Hobbies from "./Hobbies.svelte";
  import Education from "./Education.svelte";
  import Employment from "./Employment.svelte";
  import Row from "./Row.svelte";
  import Number from "./Number.svelte";
  import Instagram from "./Instagram.svelte";
  import Snapchat from "./Snapchat.svelte";
  import Artists from "./Artists.svelte";
  import Songs from "./Songs.svelte";

  export let submitted;

  let src =
    "https://th.bing.com/th/id/OIP.1Agw8tPi1oidtC_q4U4ZdgHaHa?pid=ImgDet&rs=1";
  let name = "";
  let age = "";
  let city = "";
  let state = "";
  let hobbies = [];
  let college = "";
  let major = "";
  let employment = "";
  let feet = "";
  let inches = "";
  let religion = "";
  let drinkVal = "";
  let smokeVal = "";
  let number = "";
  let instagram = "";
  let snapchat = "";
  let artists = [];
  let songs = [];

  const submit = () => {
    if (
      src ==
      "https://th.bing.com/th/id/OIP.1Agw8tPi1oidtC_q4U4ZdgHaHa?pid=ImgDet&rs=1"
    ) {
      return alert("Must upload image");
    }
    if (name == "") {
      return alert("Must include name");
    }
    if (age == "") {
      return alert("Must include age");
    }
    if (number == "" && instagram == "" && snapchat == "") {
      return alert("Must include at least one form of contact");
    }
    const application = {
      picture: { src },
      name: { name },
      age: { age },
      location: {
        city: { city },
        state: { state },
      },
      hobbies: { hobbies },
      education: {
        college: { college },
        major: { major },
      },
      employment: { employment },
      height: {
        feet: { feet },
        inches: { inches },
      },
      religion: { religion },
      drinkStatus: { drinkVal },
      smokeStatus: { smokeVal },
      contacts: {
        phoneNumber: { number },
        instagram: { instagram },
        snapchat: { snapchat },
      },
      music: {
        artists: { artists },
        songs: { songs },
      },
    };
    console.log({ application });
    add();
    submitted = true;
    window.scrollTo(0, 0);
  };
</script>

<div class="container">
  <Heading bind:src bind:name bind:age bind:city bind:state />
  <Hobbies bind:hobbies />
  <Education bind:college bind:major />
  <Employment bind:employment />
  <Row bind:feet bind:inches bind:religion bind:drinkVal bind:smokeVal />
  <Number bind:number />
  <Instagram bind:instagram />
  <Snapchat bind:snapchat />
  <Artists bind:artists />
  <Songs bind:songs />
  <div class="center">
    <button on:click={submit}>Submit Application</button>
  </div>
</div>

<style>
  .center {
    display: flex;
    justify-content: center;
  }
  button {
    background-color: #b638ff;
    color: white;
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 22px;
    padding: 5px 20px;
    border-radius: 20px;
    border: 0px;
    margin-top: 50px;
  }
  button:hover {
    background-color: rgb(192, 83, 255);
  }
</style>
