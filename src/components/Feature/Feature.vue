<script lang="ts">
export default {
    name: 'Feature',
}
</script>

<template>
    <section id="feature">
        <div class="features-container">
            <h1>
                FEATURES
            </h1>
            <h3>What Does SusCode Scan For?</h3>
            <p id="p">
            The below patterns are dangerous because they either execute code or modify content dynamically, making it easy for malicious actors to inject harmful input if proper security controls are not in place.
            </p>
        </div>

        <div class="tabs">
            <b-tabs class="b-tabs b-tab-container" content-class="mt-3">
                    <b-tab class="b-tab" title="shell_exec()" active><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, shell_exec executes shell commands directly from the code. If untrusted input is passed to it, it can lead to command injection, allowing attackers to execute arbitrary system commands.</p></b-tab>
                    <b-tab class="b-tab" title="os.system()"><p class="p"> This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, os.system runs shell commands in Python. Passing unvalidated or unsanitized user input can allow attackers to execute harmful commands, resulting in command injection.</p></b-tab>
                    <b-tab class="b-tab" title="document.write()"><p class="p">This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, document.write inserts content directly into the DOM in JavaScript. If it includes user-controlled input, it can lead to cross-site scripting (XSS) attacks, allowing malicious scripts to be executed in the user’s browser.</p></b-tab>
                    <b-tab class="b-tab" title="dangerouslySetInnerHTML()"><p class="p">This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, dangerouslySetInnerHTML is a React property that sets HTML directly in the DOM. If untrusted data is used without proper sanitization, it poses a high risk of XSS by injecting harmful HTML or scripts into the webpage.</p></b-tab>
                    <b-tab class="b-tab" title="eval()"><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, eval executes a string as JavaScript code. It can easily allow attackers to execute arbitrary code if untrusted input is passed to it, leading to code injection vulnerabilities.</p></b-tab>
                    <b-tab class="b-tab" title="exec()"><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, exec executes system commands in many programming languages (e.g., PHP, Python). Like shell_exec, it can be used for command injection if untrusted input is processed without validation.</p></b-tab>
                    <b-tab class="b-tab" title="System()"><p class="p">This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code or the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, System commands (e.g., System() in Java) allow running system-level commands. If unvalidated input is passed, it could result in command injection and compromise system security.</p></b-tab>
            </b-tabs>
        </div>
  </section>
</template>

<style lang="css" scoped>
#feature {
      width: 100vw; /* w-full */
      height: 85vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: #e8e8e8;
      background: linear-gradient(to bottom, #242424 0%, #000000 100%);
      box-sizing: border-box;
      margin: 0;
      padding: 0;
  }

  .features-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin: 20px;
  }

  p {
  width: 75%;
  text-align: center;
}

.tabs {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.b-tabs {
  display: flex;
  flex-direction: column;
  width: 100%;
  background-color: #333; /* Background color of the tabs */
  border-radius: 8px; /* Rounded corners for the tabs container */
  overflow: hidden; /* Hide overflow to maintain rounded corners */
  align-items: center;
}

.b-tab-container {
    display: flex; /* Align tabs horizontally */
    width: 100%;
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