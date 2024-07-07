import Link from 'next/link';

const Header = () => (
  <header>
    <nav className="bg-gray-800 p-4">
      <div className="container mx-auto flex justify-between items-center">
        <Link href="/">
          <a className="text-white text-2xl font-bold">My Webpage</a>
        </Link>
        <ul className="flex space-x-4">
          <li><Link href="#home"><a className="text-white">Home</a></Link></li>
          <li><Link href="#features"><a className="text-white">Features</a></Link></li>
          <li><Link href="#testimonials"><a className="text-white">Testimonials</a></Link></li>
          <li><Link href="#contact"><a className="text-white">Contact</a></Link></li>
        </ul>
      </div>
    </nav>
  </header>
);

export default Header;



const Hero = () => (
  <section id="home" className="hero bg-cover bg-center text-center text-white flex items-center" style={{ backgroundImage: "url('hero-background.jpg')", height: '100vh' }}>
    <div className="container mx-auto">
      <h1 className="text-5xl font-bold">Welcome to My Unique Webpage</h1>
      <p className="text-xl mt-4">Your solution for product management</p>
      <a href="#features" className="mt-8 inline-block bg-green-500 text-white py-2 px-4 rounded">Learn More</a>
    </div>
  </section>
);

export default Hero;



const Features = () => (
  <section id="features" className="py-16">
    <div className="container mx-auto text-center">
      <h2 className="text-3xl font-bold mb-8">Features</h2>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div>
          <h3 className="text-xl font-semibold">Feature 1</h3>
          <p className="mt-2">Description of feature 1.</p>
        </div>
        <div>
          <h3 className="text-xl font-semibold">Feature 2</h3>
          <p className="mt-2">Description of feature 2.</p>
        </div>
        <div>
          <h3 className="text-xl font-semibold">Feature 3</h3>
          <p className="mt-2">Description of feature 3.</p>
        </div>
      </div>
    </div>
  </section>
);

export default Features;



const Testimonials = () => (
  <section id="testimonials" className="py-16 bg-gray-100">
    <div className="container mx-auto text-center">
      <h2 className="text-3xl font-bold mb-8">Testimonials</h2>
      <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div>
          <p className="italic">"This is the best product ever!"</p>
          <h4 className="mt-4">- Happy Customer</h4>
        </div>
        <div>
          <p className="italic">"I can't imagine my life without it."</p>
          <h4 className="mt-4">- Satisfied User</h4>
        </div>
      </div>
    </div>
  </section>
);

export default Testimonials;





const Footer = () => (
  <footer id="contact" className="py-8 bg-gray-800 text-white text-center">
    <div className="container mx-auto">
      <h2 className="text-2xl mb-4">Contact Us</h2>
      <p>Email: info@mywebpage.com</p>
      <p>Phone: +123 456 7890</p>
      <p>&copy; 2024 My Unique Webpage. All rights reserved.</p>
    </div>
  </footer>
);

export default Footer;




import Header from '../components/Header';
import Hero from '../components/Hero';
import Features from '../components/Features';
import Testimonials from '../components/Testimonials';
import Footer from '../components/Footer';

export default function Home() {
  return (
    <div>
      <Header />
      <Hero />
      <Features />
      <Testimonials />
      <Footer />
    </div>
  );
}
