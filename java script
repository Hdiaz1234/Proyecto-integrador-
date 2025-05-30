
document.addEventListener('DOMContentLoaded', function() {
    const track = document.querySelector('.carousel-track');
    const slides = Array.from(document.querySelectorAll('.carousel-slide'));
    const prevBtn = document.querySelector('.carousel-btn.prev');
    const nextBtn = document.querySelector('.carousel-btn.next');
    let currentIndex = 0;

    
    function updateCarousel() {
        track.style.transform = `translateX(-${currentIndex * 100}%)`;
        track.style.width = `${slides.length * 100}%`;
        slides.forEach(slide => {
            slide.style.width = `${100 / slides.length}%`;
            slide.style.flex = `0 0 ${100 / slides.length}%`;
        });
    }

    if (prevBtn && nextBtn && slides.length > 0) {
        prevBtn.addEventListener('click', function(e) {
            e.preventDefault();
            currentIndex = (currentIndex === 0) ? slides.length - 1 : currentIndex - 1;
            updateCarousel();
        });
        nextBtn.addEventListener('click', function(e) {
            e.preventDefault();
            currentIndex = (currentIndex === slides.length - 1) ? 0 : currentIndex + 1;
            updateCarousel();
        });
    }
   
    updateCarousel();
    
    window.addEventListener('resize', updateCarousel);
});
