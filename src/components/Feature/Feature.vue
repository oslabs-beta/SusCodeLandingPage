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
            <p class="p">
            The below patterns are dangerous because they either execute code or modify content dynamically, making it easy for malicious actors to inject harmful input if proper security controls are not in place.
            </p>
        </div>
    </section>

    <section id="feature">
    <div>
        <b-tabs content-class="mt-3">
            <b-tab title="shell_exec()" active><p>This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, shell_exec executes shell commands directly from the code. If untrusted input is passed to it, it can lead to command injection, allowing attackers to execute arbitrary system commands.</p></b-tab>
            <b-tab title="os.system()"><p> This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, os.system runs shell commands in Python. Passing unvalidated or unsanitized user input can allow attackers to execute harmful commands, resulting in command injection.</p></b-tab>
            <b-tab title="document.write()"><p>This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, document.write inserts content directly into the DOM in JavaScript. If it includes user-controlled input, it can lead to cross-site scripting (XSS) attacks, allowing malicious scripts to be executed in the user’s browser.</p></b-tab>
            <b-tab title="dangerouslySetInnerHTML()"><p>This code pattern can introduce vulnerabilities because it allows the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, dangerouslySetInnerHTML is a React property that sets HTML directly in the DOM. If untrusted data is used without proper sanitization, it poses a high risk of XSS by injecting harmful HTML or scripts into the webpage.</p></b-tab>
            <b-tab title="eval()"><p>This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, eval executes a string as JavaScript code. It can easily allow attackers to execute arbitrary code if untrusted input is passed to it, leading to code injection vulnerabilities.</p></b-tab>
            <b-tab title="exec()"><p>This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, exec executes system commands in many programming languages (e.g., PHP, Python). Like shell_exec, it can be used for command injection if untrusted input is processed without validation.</p></b-tab>
            <b-tab title="System()"><p>This code pattern can introduce vulnerabilities because it allows the execution of arbitrary code or the insertion of content in a way that is hard to control. This makes the code within this extension vulnerable to attacks. Specifically, System commands (e.g., System() in Java) allow running system-level commands. If unvalidated input is passed, it could result in command injection and compromise system security.</p></b-tab>
        </b-tabs>
    </div>
  </section>
</template>

<style lang="css" scoped>
#feature {
      width: 100%; /* w-full */
      display: flex;
      align-items: center;
      height: 100%;
      color: #e8e8e8;
      background-color: #242424;
  }

#text {
    display: column;
    width: 100%; /* w-full */
    text-align: center;
    justify-content: center;
  }

 .description-container {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    margin: 20px;
  }

  .descriptionBox {
    width: 40%;
    border-radius: 25px;
    background: #002351;
    background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    padding: 20px;
  }

  .features-container {
    display: column;
    justify-content: space-between;
    gap: 20px;
    margin: 20px;
    align-items: center;
    justify-content: center;
  }

  .p {
    display: column;
    width: 50%;
    align-items: center;
    justify-content: center;
  }
</style>