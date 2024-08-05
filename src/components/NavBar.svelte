<script>
    export let menuSelected;
</script>

<main>
    <nav>
        <div class="container">
            <ul>
            <h1 class="menu-heading">
                TheJams
            </h1>
            <li id="icons">
                <a href="https://github.com/sophifang/tiktok-listening-party" target="_blank">
                <img 
                    src="github-mark.png" 
                    alt="GitHub Repo" 
                    title="GitHub Repo" 
                    width="35px"
                />
                </a>
            </li>
            <li id="icons">
                <a href="https://www.figma.com/proto/WhRSRwaN7Rr8fHFvNbTqGn/Designs?node-id=939-2353&t=JFR1hpJbFzYzJUaT-1&scaling=scale-down&content-scaling=fixed&page-id=327%3A1404&starting-point-node-id=939%3A2353&show-proto-sidebar=1" target="_blank">
                <img 
                    src="Figma-logo.png" 
                    alt="Figma" 
                    title="Figma Demo"
                    width="32px"/>
                </a>
            </li>
            <li id="icons">
                <button id="menu-btn" class:menuSelected on:click="{() => menuSelected = !menuSelected}">
                <svg width=33 height=26>
                    <line id="top" x1=0 y1=3  x2=30 y2=3/>
                    <line id="middle" x1=0 y1=13 x2=30 y2=13/>
                    <line id="bottom" x1=0 y1=23 x2=30 y2=23/>
                </svg>
                </button>
            </li>
            </ul>
        </div>
    </nav>
</main>

<style>
    .container{
        position: relative;
        width: 100%;
    }

    nav {
        display: flex;
        border-bottom: 0.1px solid rgba(0, 0, 0, 0.3);
        position: fixed;
        background-color: #FFFFFF;
        top: 0;
        left: 0;
        right: 0;
        z-index: 10;
    } 

    #menu-btn{
        background: none;
        color: inherit;
        border: none;
        padding: 0;
    }

    li{
        margin: auto;
    }

    ul {
        display: flex;
        margin-top: 0px;
        margin-bottom: 0px;
        padding-left: 2.5vw;
        list-style: none;
        align-items: center;
        justify-content: center;
        height: 65px;
    }


    #icons{
        width:65px;
    }

    .menu-heading{
        font-size: 40px;
        margin: 0px;
        width: 85vw;
    }
  
    svg {
        color: black;
		transition: transform 0.3s ease-in-out;
	}
	
	svg line {
		stroke: currentColor;
		stroke-width: 3;
		transition: transform 0.3s ease-in-out
	}
			
	.menuSelected #top {
		transform: translate(7px, 0px) rotate(45deg);
	}
	
	.menuSelected #middle {
		opacity: 0;
	}
	
    .menuSelected #bottom {
		transform: translate(-12px, 7px) rotate(-45deg);
	}
</style>