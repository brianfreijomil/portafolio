* prototype card
* 
<div class="project-card">
            <div class="card-content">
                <p class="card-heading">Card Hover Effect
                </p><p class="para">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi
                laboriosam at voluptas minus culpa deserunt delectus sapiente
                inventore pariatur
            </p>
                <button class="card-btn">Read more</button>
            </div>
        </div>

document.querySelectorAll(".smooth-scroll").forEach(function (link) {
link.addEventListener("click", function (e) {
e.preventDefault();

        const targetId = this.getAttribute("href").substring(1);
        const targetElement = document.getElementById(targetId);

        if (targetElement) {
            targetElement.scrollIntoView({
            });
        }
    });
});

.project-card {
position: relative;
display: flex;
align-items: center;
justify-content: center;
width: 320px;
box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
padding: 32px;
overflow: hidden;
border-radius: 10px;
transition: all 0.5s cubic-bezier(0.23, 1, 0.320, 1);
background-image: url("img/Captura de pantalla 2023-11-03 181756.png");
background-size: cover;
}

.card-content {
display: flex;
flex-direction: column;
align-items: flex-start;
gap: 20px;
color: #e8e8e8;
transition: all 0.5s cubic-bezier(0.23, 1, 0.320, 1);
}

.card-content .card-heading {
font-weight: 700;
font-size: 32px;
}

.card-content .para {
line-height: 1.5;
}

.card-content .card-btn {
color: #e8e8e8;
text-decoration: none;
padding: 10px;
font-weight: 600;
border: none;
cursor: pointer;
background: linear-gradient(-45deg, #8126f5 0%, #4fdab0 100% );
border-radius: 5px;
box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.project-card::before {
content: "";
position: absolute;
left: 0;
bottom: 0;
width: 100%;
height: 5px;
background: linear-gradient(-45deg, #8126f5 0%, #4fdab0 100% );
z-index: -1;
transition: all 0.5s cubic-bezier(0.23, 1, 0.320, 1);
}

.project-card:hover::before {
height: 100%;
}

.project-card:hover {
box-shadow: none;
}

.project-card:hover .btn {
color: #212121;
background: #e8e8e8;
}

.card-content .card-btn:hover {
outline: 2px solid #e8e8e8;
background: transparent;
color: #e8e8e8;
}

.card-content .card-btn:active {
box-shadow: none;
}