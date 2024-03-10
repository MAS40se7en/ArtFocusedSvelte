<script lang="ts">
    import { Home, MagnifyingGlass } from "svelte-radix";
    import {
        DropdownMenu,
        DropdownMenuContent,
        DropdownMenuItem,
        DropdownMenuPortal,
        DropdownMenuLabel,
        DropdownMenuSeparator, DropdownMenuSubTrigger,
        DropdownMenuTrigger,
    } from "$lib/components/ui/dropdown-menu";
    import DropdownMenuSubContent from '$lib/components/ui/dropdown-menu/dropdown-menu-sub-content.svelte';
    import { DropdownMenuRadioGroup } from '$lib/components/ui/dropdown-menu/index.js';

    const navbarOptions = [
        {
            icon:Home,
            title:Home,
            href:'/'
        },
        {
            icon:MagnifyingGlass,
            title:MagnifyingGlass
        }
    ]

</script>


<div class="bar gap-4 px-4 md:mx-auto flex justify-between rounded-full">
    <a href="/" class="m-auto"><Home /></a>
    <a class="m-auto" href="/artists">Artists</a>
    <DropdownMenu>
        <DropdownMenuTrigger>Categories</DropdownMenuTrigger>
        <DropdownMenuContent>
            <DropdownMenuRadioGroup>
            <DropdownMenuItem>Digital</DropdownMenuItem>
            <DropdownMenuItem>Modern</DropdownMenuItem>
            <DropdownMenuItem>Pencil</DropdownMenuItem>
            <DropdownMenuItem>Academic</DropdownMenuItem>
            </DropdownMenuRadioGroup>
            <DropdownMenuSeparator/>
            <DropdownMenuRadioGroup class="ml-2 border-l-2 border-gray-500 my-2">
                <DropdownMenuItem>tag</DropdownMenuItem>
            </DropdownMenuRadioGroup>
        </DropdownMenuContent>
    </DropdownMenu>
    <div class="input flex bg-dark rounded-full w-auto">
        <input type="text" placeholder="Search" class="px-3 rounded-full mr-0.9 hidden md:inline-block" >
        <button class="w-10 pl-2">
            <MagnifyingGlass/>
        </button>
    </div>
    <button>Login</button>
    <button>Register</button>
</div>

<style>
    .bar{
        width: fit-content;
        margin-top: 1rem;
        position: sticky;
        z-index: 1000;
        background-color: rgba(31, 31, 31, 0.9);
        align-items: center;
        display: flex;
        height: 55px;
        backdrop-filter: blur(5px);
    }

    .input {
        background-color: rgb(153, 122, 19);
        height: 40px;
    }

    input {
        background-color: transparent;
        width:89%;
        transition: 0.3s;
    }

    input::placeholder {
        color: white;
    }

    input:focus {
        background-color: rgb(196, 177, 26, 0.5);
        outline: none;
        color: rgba(31, 31, 31, 0.9);
        font-weight: 500;
    }


</style>
