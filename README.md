@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@500&family=Roboto:wght@500&display=swap");

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

:root {
    --primary-text-color: #1d374a;
    --secondary-text-color: #282f36;
    --accent-color: #103754;
    --accent-color-dark: #172b3b;
}

html{
    overflow-x: hidden;
}
body {
    overflow-x: hidden;
    font-family: "Poppins", sans-serif;
    color: var(--primary-text-color);
    background-color: #e1cbcb;
}

p {
    font-family: "Roboto", sans-serif;
    color: var(--secondary-text-color);
    line-height: 1.4rem;
}

a {
    text-decoration: none;
}

ul {
    list-style: none;
}

.flex {
    display: flex;
    align-items: center;
}

.container {
    max-width: 1180px;
    margin-inline: auto;
    overflow: hidden;
}

nav {
    background-color: #e4f4ff;
    box-shadow: 0 0 4px #bbd0e2;
    position: fixed;
    top: 0;
    z-index: 99;
    left: 0;
    right: 0;   
}

.main-nav {
    justify-content: space-between;
    padding-block: 8px;
    height: 75px;
    margin-left: 150px;
    margin-right: 10px;
}

.company-logo img {
    width: 120px;
}

.nav-links ul {
    gap: 16px;
}

.hover-link {
    cursor: pointer;
}

.hover-link:hover {
    color: var(--secondary-text-color);
}

.hover-link:active {
    color: red;
}

.nav-item.active {
    color: var(--accent-color);
}

.search-bar {
    height: 32px;
    gap: 8px;
}

.news-input {
    width: 200px;
    height: 100%;
    padding-inline: 12px;
    border-radius: 4px;
    border: 2px solid #bbd0e2;
    font-family: "Roboto", sans-serif;
}

.search-button {
    background-color: var(--accent-color);
    color: white;
    padding: 8px 24px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-family: "Roboto", sans-serif;
}

.search-button:hover {
    background-color: var(--accent-color-dark);
}

main {
    padding-block: 20px;
    margin-top: 80px;
}

.cards-container {
    justify-content: space-between;
    flex-wrap: wrap;
    row-gap: 20px;
    column-gap: 20px;
    align-items: center;
    pointer-events: auto;
}

.card {
    width: 360px;
    min-height: 400px;
    box-shadow: 0 0 4px #d4ecff;
    border-radius: 4px;
    cursor: pointer;
    background-color: #e1cbcb;
    overflow: hidden;
    transition: all 0.3s ease;
}

.card:hover {
    box-shadow: 1px 1px 8px #000000;
    background-color: #ccdee7;
    transform: translateY(-2px);
}

.card-header img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.card-content {
    padding: 12px;
}

.news-source {
    margin-block: 12px;
}


.searching{
    display: none;
    margin-right: 10px;
}
.searching-img{
    width: 17px;
    color: var(--accent-color);
}


/* responsiveness of webapp  */
@media (max-width:1120px){
    .cards-container{
        margin-left: 13px;
        margin-right: 13px;
        justify-content: space-evenly;
        align-items: center;
        column-gap: 13px;
    }
    .main-nav{
        margin-left: 10px;
    }
}
@media (max-width: 750px){

    .cards-container{
        margin-left: 10px;
        margin-right: 10px;
        justify-content: space-evenly;
        align-items: center;
        column-gap: 13px;
    }
    .nav-links{
        display: none;
    }
    .searching{
        display: block;
    }
    .searched{
        transform: translateX(100%);
        transition: all 0.23s linear;
        opacity: 0;
        visibility: hidden;
        pointer-events: none;
    }
    .activeresp .searched{
        transform: translateX(0);
        transition: all 0.23s linear;
        opacity: 1;
        visibility: visible;
        pointer-events: auto;
    }
    .activeresp .searching{
        display: none;
    }
}

@media (max-width:431px){
    .searched{
        display: flex;
        flex-direction: column;
        align-items:end;
    }
    .search-button {
    background-color: var(--accent-color);
    color: white;
    padding: 8px 24px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-family: "Roboto", sans-serif;
    width: 90px;
}

.search-button:hover {
    background-color: var(--accent-color-dark);
}
}
