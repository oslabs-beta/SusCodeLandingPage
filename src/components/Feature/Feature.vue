<script lang="ts">
export default {
    name: 'Feature',
}
</script>

<template>
    <section id="features">
        <div class="features-container">
            <span class="features-heading">FEATURES</span>
             <h3>What Does SusCode Scan For?</h3>
        </div>
            
        <section class="types">
            <div class="row">
                <span class="works-span">Common security risk functions via static analysis</span>
                <img src="../../assets/images/arrow.gif" class="gif small-arrow" alt="Arrow Gif" />
                <span class="works-span">SusCode reads the extension files locally and scans for code patterns that may introduce vulnerabilities.</span>
            </div>
            
            <div class="row">
                <span class="works-span">Use of telemetry</span>
                <img src="../../assets/images/arrow.gif" class="gif small-arrow" alt="Arrow Gif" />
                <span class="works-span">SusCode scans HTTP requests and shows where the request is made in the code.</span>
            </div>
            
            <div class="row">
                <span class="works-span">Dependencies installed in packages</span>
                <img src="../../assets/images/arrow.gif" class="gif small-arrow" alt="Arrow Gif" />
                <span class="works-span">SusCode runs package dependencies through the OSV API to detect vulnerabilities.</span>
            </div>
        </section>

        <div class="scans">
            <h1>SCANS</h1>
            <hr>
            <p>The below patterns are potentially dangerous because they either execute code or modify content dynamically, making it easy for malicious actors to inject harmful input if proper security controls are not in place.</p>
        </div>

        <div class="tabs">
            <b-tabs class="b-tabs b-tab-container" content-class="mt-3">
                    <b-tab class="b-tab" title="shell_exec()" active><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, shell_exec executes shell commands directly from the code. If untrusted input is passed to it, it can lead to command injection, allowing attackers to execute arbitrary system commands.</p></b-tab>
                    <b-tab class="b-tab" title="os.system()"><p class="p"> This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, os.system runs shell commands in Python. Passing unvalidated or unsanitized user input can allow attackers to execute harmful commands, resulting in command injection.</p></b-tab>
                    <b-tab class="b-tab" title="document.write()"><p class="p">This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, document.write inserts content directly into the DOM in JavaScript. If it includes user-controlled input, it can lead to cross-site scripting (XSS) attacks, allowing malicious scripts to be executed in the user’s browser.</p></b-tab>
                    <b-tab class="b-tab" title="dangerouslySetInnerHTML()"><p class="p">This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, dangerouslySetInnerHTML is a React property that sets HTML directly in the DOM. If untrusted data is used without proper sanitization, it poses a high risk of XSS by injecting harmful HTML or scripts into the webpage.</p></b-tab>
                    <b-tab class="b-tab" title="eval()"><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, eval executes a string as JavaScript code. It can easily allow attackers to execute arbitrary code if untrusted input is passed to it, leading to code injection vulnerabilities.</p></b-tab>
                    <b-tab class="b-tab" title="System()"><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code or the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, System commands (e.g., System() in Java) allow running system-level commands. If unvalidated input is passed, it could result in command injection and compromise system security.</p></b-tab>
            </b-tabs>
        </div>
  </section>
</template>

<style lang="css" scoped>
#features {
      width: 100vw; /* w-full */
      padding-top: 150px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: #e8e8e8;
      background: linear-gradient(to bottom, #242424 0%, #000000 100%);
      box-sizing: border-box;
      margin: 0;
  }

  .features-heading {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

  .features-container {
    width: 75%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .types {
  display: grid;
  grid-template-rows: auto auto auto; /* Three rows: boxes, arrows, boxes */
  grid-template-columns: repeat(3, 1fr); /* Three equal-width columns */
  gap: 3em; /* Gap between items */
  justify-items: center; /* Center items horizontally within each grid cell */
  align-items: center; /* Center items vertically */
  margin: 0 auto; /* Center the grid itself */
  padding: 2em; /* Adjust padding if needed */
  max-width: 1200px; /* Optional: limit the width so content doesn't stretch too far */
  width: 100%;
  box-sizing: border-box; /* Ensure padding is included within the width */
}

.works-span {
  background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  border-radius: 10px;
  width: 90%; /* Control box width */
  padding: 2.5em; /* Increase padding for larger size */
  text-align: center;
  font-size: 1.5rem; /* Increase font size */
  color: #fff;
  box-shadow: 0px 10px 30px rgb(0, 44, 94), 0px 10px 30px #fff;
}

.gif.small-arrow {
  width: 75px; /* Arrow size */
  height: 75px;
}

.row {
  display: flex;
  flex-direction: column;
  align-items: center; /* Center items within the row */
  justify-content: center; /* Center row content */
  width: 100%; /* Ensure rows take up the full width */
}

.scans {
    text-align: center;
    align-items: center;
    justify-content: center;
    width: 75%;
}
  .scan {
    height: 200px;
    width: 250px;
    background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 2em;
    box-shadow: 0px 5px 20px rgb(0, 44, 94), 0px 5px 20px #fff;
    transition: all ease 0.5s;
    color: #fff;
  }

  .scan:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
  }

  .scan span {
    font-size: 1rem;
    font-weight: 600;
    text-align: center;
  }


.tabs {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.b-tab-container {
    display: flex; /* Align tabs horizontally */
    width: 75%;
}

.b-tabs {
  display: flex;
  flex-direction: column;
  background-color: #333; /* Background color of the tabs */
  border-radius: 8px; /* Rounded corners for the tabs container */
  overflow: hidden; /* Hide overflow to maintain rounded corners */
  align-items: center;
  font-size: 1.25em;
  padding: 0.5em;
}

/* Style for each tab header */
.b-tab {
  background-color: #444; /* Background color of the tab headers */
  color: #e8e8e8; /* Text color for the tab headers */
  border: none; /* Remove default border */
  padding: 10px 20px; /* Padding inside each tab header */
  cursor: pointer; /* Change cursor to pointer on hover */
  border-radius: 8px; /* Rounded corners for each tab header */
  flex: 1;
  text-align: center;
  display: flex;
  justify-content: center;
  /* font-size: 1.25em; */
  padding: 1.5em;
}

/* Style for the active tab header */
.b-tab.active {
  background-color: #222; /* Different background color for the active tab */
  color: #fff; /* Text color for the active tab */
}

/* Style for the tab content */
.b-tab-content {
  background-color: #222; /* Background color of the tab content */
  border-radius: 8px; /* Rounded corners for the tab content */
  padding: 20px; /* Padding inside the tab content */
  color: #e8e8e8; /* Text color inside the tab content */
  text-align: center; /* Center text in the content */
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>