import React from 'react';

const App = () => {
  const movements = [
    { name: "UNIÓN DE ENFERMOS", description: "Movimiento dedicado a la santificacion personal de los enfermos.", contact: "87 12 80 80 84", logo: "https://images.app.goo.gl/P8AJ5dA88VvkxqbWA" },
    { name: "JESUS SALVA A MI FAMILIA", description: "Grupo enfocado a la restauración de matrimonios.", contact: "87 15 34 44 57", logo: "https://images.app.goo.gl/qUGrmG5KLwSbJJfHA" },
    { name: "DIVINA MISERICORDIA", description: "Promueve la devoción a la Divina Misericordia a través de actividades espirituales.", contact: "divinamisericordia@example.com", logo: "https://placehold.co/150x150?text=Logo+DM" },
    { name: "CONQUISTANDO LAS NACIONES PARA CRISTO", description: "Movimiento misionero de Renovación Carismática que busca evangelizar a nivel nacional e internacional.", contact: "misiones@conquistandonaciones.org", logo: "https://placehold.co/150x150?text=Logo+CLN" },
    { name: "CECAF", description: "Centro de Capacitación y Formación para líderes católicos.", contact: "formacion@cecaf.org", logo: "https://placehold.co/150x150?text=Logo+CECAF" },
    { name: "RENOVACION", description: "Movimiento de Renovación Carismática Católica.", contact: "renovacion@carismatica.org", logo: "https://placehold.co/150x150?text=Logo+RC" },
    { name: "ORDEN SEGLAR CARMELITAS", description: "Comunidad seglar inspirada en la espiritualidad carmelita.", contact: "carmelitasseglares@example.com", logo: "https://placehold.co/150x150?text=Logo+OSC" },
    { name: "FOCOLARES", description: "Movimiento ecuménico que promueve la unidad entre los cristianos.", contact: "focolares@example.com", logo: "https://placehold.co/150x150?text=Logo+Focolares" },
    { name: "REGNUM CHRISTI", description: "Movimiento apostólico que busca formar líderes comprometidos con el Evangelio.", contact: "regnumchristi@example.com", logo: "https://placehold.co/150x150?text=Logo+RC" },
    { name: "UNIÓN FEMENIL CATÓLICA", description: "Asociación de mujeres católicas comprometidas con la fe y el servicio.", contact: "ufc@example.com", logo: "https://placehold.co/150x150?text=Logo+UFC" },
    { name: "ORDEN FRANCISCANA SEGLAR", description: "Comunidad seglar inspirada en la espiritualidad franciscana.", contact: "franciscanosseglares@example.com", logo: "https://placehold.co/150x150?text=Logo+OFS" },
    { name: "CABALLEROS DE COLÓN", description: "Organización fraternal católica dedicada al servicio comunitario.", contact: "caballerosdecolon@example.com", logo: "https://placehold.co/150x150?text=Logo+KC" },
    { name: "SEMBRADORES", description: "Grupo dedicado a sembrar la palabra de Dios en comunidades marginadas.", contact: "sembradores@example.com", logo: "https://placehold.co/150x150?text=Logo+Sembradores" },
    { name: "ADORACIÓN NOCTURNA", description: "Movimiento de adoración eucarística durante la noche.", contact: "adoracionnocturna@example.com", logo: "https://placehold.co/150x150?text=Logo+AN" },
    { name: "LLAMA DE AMOR", description: "Movimiento espiritual centrado en la devoción al Sagrado Corazón de Jesús.", contact: "llamadeamor@example.com", logo: "https://placehold.co/150x150?text=Logo+LA" },
    { name: "VIRGEN PEREGRINA", description: "Movimiento que promueve la devoción a la Virgen María a través de imágenes peregrinas.", contact: "virgenperegrina@example.com", logo: "https://placehold.co/150x150?text=Logo+VP" },
    { name: "SCHOENSTATT", description: "Movimiento internacional basado en la espiritualidad de Schoenstatt.", contact: "schoenstatt@example.com", logo: "https://placehold.co/150x150?text=Logo+Schoenstatt" },
  ];

  return (
    <div className="min-h-screen bg-gray-100 font-sans">
      {/* Header */}
      <header className="bg-blue-800 text-white py-4">
        <div className="container mx-auto px-4 flex justify-between items-center">
          <h1 className="text-2xl font-bold">Movimientos Laicos - Diócesis de Torreón</h1>
          <nav>
            <ul className="flex space-x-4">
              <li><a href="#about" className="hover:text-blue-300">Acerca de</a></li> 
              <li><a href="#movements" className="hover:text-blue-300">Movimientos</a></li>
              <li><a href="#contact" className="hover:text-blue-300">Contacto</a></li>
            </ul>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="bg-blue-700 text-white py-16">
        <div className="container mx-auto px-4 text-center">
          <h2 className="text-4xl font-bold mb-4">Bienvenidos a los Movimientos Laicos</h2>
          <p className="text-lg">Descubre cómo cada movimiento contribuye al desarrollo espiritual y social de nuestra comunidad.</p>
        </div>
      </section>

      {/* Movements Section */}
      <section id="movements" className="py-16">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl font-bold text-center mb-8">Movimientos Laicos</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {movements.map((movement, index) => (
              <div key={index} className="bg-white shadow-lg rounded-lg overflow-hidden transition-transform hover:scale-105">
                <img src={movement.logo} alt={`${movement.name} logo`} className="w-full h-48 object-cover" />
                <div className="p-6">
                  <h3 className="text-xl font-bold mb-2">{movement.name}</h3>
                  <p className="text-gray-700 mb-4">{movement.description}</p>
                  <p className="text-blue-600"><strong>Contacto:</strong> {movement.contact}</p>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="bg-blue-800 text-white py-8">
        <div className="container mx-auto px-4 text-center">
          <p>&copy; 2023 Diócesis de Torreón. Todos los derechos reservados.</p>
          <p>Contáctenos: contacto@diocesisdetorreon.org</p>
        </div>
      </footer>
    </div>
  );
};

export default App;- 👋 Hi, I’m @Queteimporta71
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Queteimporta71/Queteimporta71 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
