# Bakery-Website
Web development assignment

<script>



        // Mobile menu toggle
        const navToggle = document.querySelector('.mobile-nav-toggle');
        const navItems = document.querySelector('.nav-items');
        if (navToggle && navItems) {
            navToggle.addEventListener('click', () => {
                const expanded = navToggle.getAttribute('aria-expanded') === 'true';
                navToggle.setAttribute('aria-expanded', String(!expanded));
                navItems.classList.toggle('show');
                navToggle.classList.toggle('active');
            });
            // close when clicking outside
            document.addEventListener('click', (e) => {
                if (!e.target.closest('.navbar')) {
                    navItems.classList.remove('show');
                    navToggle.classList.remove('active');
                    navToggle.setAttribute('aria-expanded', 'false');
                }
            });
        }
    

    </script>