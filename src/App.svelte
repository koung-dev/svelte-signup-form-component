
<script>
    let name = ''
    let email = ''
    let password = ''
    let form = true
    let inputState = {
        nameIsActive: false,
        emailIsActive: false,
        passwordIsActive: false
    }

</script>

<!-- <div class="bg-black w-screen h-screen"> -->

    <main class="xl:main main-mobile">
        <div class="container">
            <div class="space-y-2">
                <h1 class="text-white text-2xl">Sign UP</h1>
                <p class="text-xs">it's quick & simple</p>
            </div>
    
            <div class="group h-20 relative flex flex-row items-center">
                <label for='name' class={inputState.nameIsActive || name != '' ? 'label-active' : 'label'}> name </label>
                <svg class="absolute group-hover:stroke-white" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 256 256"><path fill="currentColor" d="M230.92 212c-15.23-26.33-38.7-45.21-66.09-54.16a72 72 0 1 0-73.66 0c-27.39 8.94-50.86 27.82-66.09 54.16a8 8 0 1 0 13.85 8c18.84-32.56 52.14-52 89.07-52s70.23 19.44 89.07 52a8 8 0 1 0 13.85-8M72 96a56 56 0 1 1 56 56a56.06 56.06 0 0 1-56-56"/></svg>
                <input required bind:value={name} on:blur={() => inputState.nameIsActive = false} on:focus={() => inputState.nameIsActive = true} type="name" id="name" class="input-css">
            </div>

            <div class="group h-20 relative flex flex-row items-center">
                <button class={inputState.emailIsActive || email != '' ? 'label-active' : 'label'}> email </button>
                <svg class="absolute group-hover:stroke-white" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="currentColor" d="M13 19c0-.34.04-.67.09-1H4V8l8 5l8-5v5.09c.72.12 1.39.37 2 .72V6c0-1.1-.9-2-2-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h9.09c-.05-.33-.09-.66-.09-1m7-13l-8 5l-8-5zm0 16v-2h-4v-2h4v-2l3 3z"/></svg>
                <input bind:value={email} on:blur={() => inputState.emailIsActive = false} on:focus={() => inputState.emailIsActive = true} type="email" id="email" class="input-css">
            </div>

            <div class="group h-20 relative flex flex-row items-center">
                <button class={inputState.passwordIsActive || password != '' ? 'label-active' : 'label'}> password </button>
                <svg class="absolute group-hover:stroke-white" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="currentColor" d="M9 16a1 1 0 1 1-2 0a1 1 0 0 1 2 0m4 0a1 1 0 1 1-2 0a1 1 0 0 1 2 0m3 1a1 1 0 1 0 0-2a1 1 0 0 0 0 2"/><path fill="currentColor" fill-rule="evenodd" d="M5.25 8v1.303c-.227.016-.44.036-.642.064c-.9.12-1.658.38-2.26.981c-.602.602-.86 1.36-.981 2.26c-.117.867-.117 1.97-.117 3.337v.11c0 1.367 0 2.47.117 3.337c.12.9.38 1.658.981 2.26c.602.602 1.36.86 2.26.982c.867.116 1.97.116 3.337.116h8.11c1.367 0 2.47 0 3.337-.116c.9-.122 1.658-.38 2.26-.982c.602-.602.86-1.36.982-2.26c.116-.867.116-1.97.116-3.337v-.11c0-1.367 0-2.47-.116-3.337c-.122-.9-.38-1.658-.982-2.26c-.602-.602-1.36-.86-2.26-.981a10.215 10.215 0 0 0-.642-.064V8a6.75 6.75 0 0 0-13.5 0M12 2.75A5.25 5.25 0 0 0 6.75 8v1.253c.373-.003.772-.003 1.195-.003h8.11c.423 0 .822 0 1.195.003V8c0-2.9-2.35-5.25-5.25-5.25m-7.192 8.103c-.734.099-1.122.28-1.399.556c-.277.277-.457.665-.556 1.4c-.101.755-.103 1.756-.103 3.191c0 1.435.002 2.436.103 3.192c.099.734.28 1.122.556 1.399c.277.277.665.457 1.4.556c.754.101 1.756.103 3.191.103h8c1.435 0 2.436-.002 3.192-.103c.734-.099 1.122-.28 1.399-.556c.277-.277.457-.665.556-1.4c.101-.755.103-1.756.103-3.191c0-1.435-.002-2.437-.103-3.192c-.099-.734-.28-1.122-.556-1.399c-.277-.277-.665-.457-1.4-.556c-.755-.101-1.756-.103-3.191-.103H8c-1.435 0-2.437.002-3.192.103" clip-rule="evenodd"/></svg>                <input bind:value={password} on:blur={() => inputState.passwordIsActive = false} on:focus={() => inputState.passwordIsActive = true} type="password" id="password" class="input-css">
            </div>

            
            <div class="space-y-4">
                <div class="flex items-center space-x-2">
                    <h1 class="text-sm text-white/50">signed up already ?</h1>
                    <h1 class="text-sm text-white">Login here</h1>
                </div>
        
                <div class="flex items-center justify-around p-6 bg-white/20 text-white h-16">
                    <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 16 16"><path fill="currentColor" fill-rule="evenodd" d="M7.976 0A7.977 7.977 0 0 0 0 7.976c0 3.522 2.3 6.507 5.431 7.584c.392.049.538-.196.538-.392v-1.37c-2.201.49-2.69-1.076-2.69-1.076c-.343-.93-.881-1.175-.881-1.175c-.734-.489.048-.489.048-.489c.783.049 1.224.832 1.224.832c.734 1.223 1.859.88 2.3.685c.048-.538.293-.88.489-1.076c-1.762-.196-3.621-.881-3.621-3.964c0-.88.293-1.566.832-2.153c-.05-.147-.343-.978.098-2.055c0 0 .685-.196 2.201.832c.636-.196 1.322-.245 2.007-.245s1.37.098 2.006.245c1.517-1.027 2.202-.832 2.202-.832c.44 1.077.146 1.908.097 2.104a3.16 3.16 0 0 1 .832 2.153c0 3.083-1.86 3.719-3.62 3.915c.293.244.538.733.538 1.467v2.202c0 .196.146.44.538.392A7.98 7.98 0 0 0 16 7.976C15.951 3.572 12.38 0 7.976 0" clip-rule="evenodd"/></svg>
                    <h1 class="text-sm">KOUNG-DEV</h1>
                </div>
            </div>
        </div>
    </main>

<!-- </div> -->

