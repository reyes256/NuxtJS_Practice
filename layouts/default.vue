<template>
    <div>
        <nav>
            <ul class="nav">
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="test">test</NuxtLink></li>
                <li><NuxtLink to="welcome">welcome</NuxtLink></li>
            </ul>
        </nav>

        <slot />
    </div>
</template>