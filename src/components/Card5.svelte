<div class="card-container">
    <h1 class="card-title">Comment</h1>
    <textarea placeholder="Your feedback..." class="feedback-textarea"></textarea>
    <button aria-label="Send feedback" class="feedback-button">
        <svg xmlns="http://www.w3.org/2000/svg" height="20px" viewBox="0 0 512 512">
            <path d="M464 256A208 208 0 1 0 48 256a208 208 0 1 0 416 0zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256zm177.6 62.1C192.8 334.5 218.8 352 256 352s63.2-17.5 78.4-33.9c9-9.7 24.2-10.4 33.9-1.4s10.4 24.2 1.4 33.9c-22 23.8-60 49.4-113.6 49.4s-91.7-25.5-113.6-49.4c-9-9.7-8.4-24.9 1.4-33.9s24.9-8.4 33.9 1.4zM144.4 208a32 32 0 1 1 64 0 32 32 0 1 1 -64 0zm192-32a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"></path>
        </svg>
    </button>
    <button aria-label="Alternate feedback" class="feedback-button">
        <svg xmlns="http://www.w3.org/2000/svg" height="20px" viewBox="0 0 512 512">
            <path d="M464 256A208 208 0 1 0 48 256a208 208 0 1 0 416 0zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256zM174.6 384.1c-4.5 12.5-18.2 18.9-30.7 14.4s-18.9-18.2-14.4-30.7C146.9 319.4 198.9 288 256 288s109.1 31.4 126.6 79.9c4.5 12.5-2 26.2-14.4 30.7s-26.2-2-30.7-14.4C328.2 358.5 297.2 336 256 336s-72.2 22.5-81.4 48.1zM144.4 208a32 32 0 1 1 64 0 32 32 0 1 1 -64 0zm192-32a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"></path>
        </svg>
    </button>
    <span class="spacer"></span>
    <button aria-label="Custom action" class="custom-action-button">
        <svg fill="none" viewBox="0 0 24 24" height="30px" width="30px" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linejoin="round" stroke-linecap="round" stroke-width="1.5" d="M7.39999 6.32003L15.89 3.49003C19.7 2.22003 21.77 4.30003 20.51 8.11003L17.68 16.6C15.78 22.31 12.66 22.31 10.76 16.6L9.91999 14.08L7.39999 13.24C1.68999 11.34 1.68999 8.23003 7.39999 6.32003Z"></path>
            <path stroke-linejoin="round" stroke-linecap="round" stroke-width="1.5" d="M10.11 13.6501L13.69 10.0601"></path>
        </svg>
    </button>
</div>

<style>
.card-container {
    width: 350px;
    height: 270px;
    background-color: white;
    border: 1px solid #e2e8f0;
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 0.5rem;
    border-radius: 0.75rem;
    padding: 0.5rem;
    font-size: 0.875rem;
    font-family: Funnel Display;
    position: absolute;
    top: 80%;
    left: 13%;
}

.card-title {
    text-align: center;
    color: #000000;
    font-size: 1.25rem;
    font-weight: bold;
    grid-column: span 6;
}

.feedback-textarea {
    background-color: #f9f9f9;
    color: #475569;
    height: 7rem;
    border: 1px solid #e2e8f0;
    grid-column: span 6;
    resize: none;
    outline: none;
    border-radius: 0.5rem;
    padding: 0.5rem;
    transition: border-color 0.3s;
}

.feedback-textarea::placeholder {
    color: #475569;
    opacity: 0.5;
}
.feedback-textarea:hover {
    border-color: #475569;
}
.feedback-textarea:focus {
    border-color: #475569;
}

.feedback-button {
    fill: #475569;
    grid-column: span 1;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 0.5rem;
    padding: 0.5rem;
    transition: background-color 0.3s, border-color 0.3s;
    background-color: #f9f9f9;
    border: 1px solid #e2e8f0;
}

.feedback-button:hover {
    border-color: #475569;
}

.feedback-button:focus {

    border-color: #000000;
}

.spacer {
    grid-column: span 2;
}

.custom-action-button {
    background-color: #f9f9f9;
    stroke: #475569;
    border: 1px solid #e2e8f0;
    grid-column: span 2;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 0.5rem;
    transition: background-color 0.3s, border-color 0.3s, color 0.3s;
}
.custom-action-button:hover {
    border-color: #000000;
    
}
.custom-action-button:focus {
    
    border-color: #000000;
    
}


</style>