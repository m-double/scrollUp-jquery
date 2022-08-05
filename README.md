# scrollUp
scroll up button jquery


![Captura1](https://user-images.githubusercontent.com/56656263/181730734-d772462f-8078-4d70-90a3-b46df061b489.PNG)

## html
``` html
        <img src="img/bt-up.svg" id="btn-top" alt="scrollUp">
        <script src="https://code.jquery.com/jquery-3.6.0.min.js"
        integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>

    <script>
        let toTopVisible = false;
        document.addEventListener('DOMContentLoaded', function () {
            window.onscroll = function () {
                if (window.scrollY >= 500) {
                    if (!toTopVisible) {
                        $('#btn-top').addClass('visible');
                    }
                    toTopVisible = true;
                } else if (window.scrollY < 500) {
                    $('#btn-top').removeClass('visible');
                    toTopVisible = false;
                }
            };
            $(document).on('click', '#btn-top', function () {
                $(this).blur();
                window.scroll({
                    top: 0,
                    left: 0,
                    behavior: 'smooth'
                });
            });
        });
    </script> 
```

## css
``` css
#btn-top {
    position: fixed;
    bottom: 50px;
    right: 50px;
    display: none;
}
#btn-top.visible {
    position: fixed;
    bottom: 50px;
    right: 50px;
    display: block;
}
```
## svg
``` svg
<svg xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="50px" viewBox="0 0 24 24" width="50px" fill="#000000">
<g>
<rect fill="none" height="24" width="24"/>
<path d="M12,20c-4.41,0-8-3.59-8-8s3.59-8,8-8s8,3.59,8,8S16.41,20,12,20 M12,22c5.52,0,10-4.48,10-10c0-5.52-4.48-10-10-10 C6.48,2,2,6.48,2,12C2,17.52,6.48,22,12,22L12,22z M11,12l0,4h2l0-4h3l-4-4l-4,4H11z"/>
</g>
</svg>
```
