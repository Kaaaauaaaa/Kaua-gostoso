# Kaua-gostoso
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kaua Gostoso - Assista filmes grátis com amigos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .movie-card:hover .movie-overlay {
            opacity: 1;
            transform: translateY(0);
        }
        .movie-overlay {
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateY(20px);
        }
        .watch-party-btn {
            transition: all 0.3s ease;
        }
        .watch-party-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(255, 0, 100, 0.3);
        }
        .hero-gradient {
            background: linear-gradient(135deg, #ff4d4d 0%, #f9cb28 100%);
        }
        .genre-tag {
            transition: all 0.2s ease;
        }
        .genre-tag:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .search-bar:focus {
            box-shadow: 0 0 0 3px rgba(255, 0, 100, 0.3);
        }
        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }
        .animate-pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
    </style>
</head>
<body class="bg-gray-900 text-white min-h-screen">
    <!-- Header/Navbar -->
    <header class="bg-gray-800 shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-film text-2xl text-pink-500"></i>
                <h1 class="text-2xl font-bold bg-gradient-to-r from-pink-500 to-yellow-400 bg-clip-text text-transparent">Kaua Gostoso</h1>
            </div>
            
            <div class="hidden md:flex items-center space-x-6">
                <a href="#" class="hover:text-pink-400 transition">Início</a>
                <a href="#" class="hover:text-pink-400 transition">Filmes</a>
                <a href="#" class="hover:text-pink-400 transition">Séries</a>
                <a href="#" class="hover:text-pink-400 transition">Sobre</a>
            </div>
            
            <div class="flex items-center space-x-4">
                <div class="relative">
                    <input type="text" placeholder="Buscar filmes..." class="search-bar bg-gray-700 rounded-full py-1 px-4 pl-10 focus:outline-none focus:ring-2 focus:ring-pink-500 w-40 md:w-64">
                    <i class="fas fa-search absolute left-3 top-2 text-gray-400"></i>
                </div>
                <button class="bg-pink-600 hover:bg-pink-700 px-4 py-1 rounded-full flex items-center space-x-1 watch-party-btn">
                    <i class="fas fa-user-friends"></i>
                    <span class="hidden md:inline">Assistir Juntos</span>
                </button>
            </div>
            
            <button class="md:hidden text-2xl">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero-gradient py-16 md:py-24">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h2 class="text-4xl md:text-5xl font-bold mb-4">Assista filmes grátis com quem você ama</h2>
                <p class="text-xl mb-6">No Kaua Gostoso você encontra os melhores filmes para assistir com amigos, família ou sua namorada. Tudo 100% gratuito!</p>
                <div class="flex space-x-4">
                    <button class="bg-white text-pink-600 px-6 py-2 rounded-full font-bold hover:bg-gray-100 transition watch-party-btn">
                        Começar agora
                    </button>
                    <button class="border-2 border-white text-white px-6 py-2 rounded-full font-bold hover:bg-white hover:text-pink-600 transition">
                        Como funciona?
                    </button>
                </div>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <div class="relative w-full max-w-md">
                    <div class="absolute -top-6 -left-6 w-32 h-32 bg-yellow-400 rounded-lg opacity-20 animate-pulse"></div>
                    <div class="absolute -bottom-6 -right-6 w-32 h-32 bg-pink-500 rounded-lg opacity-20 animate-pulse"></div>
                    <img src="https://images.unsplash.com/photo-1536440136628-849c177e76a1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1025&q=80" alt="Pessoas assistindo filme juntas" class="rounded-lg shadow-2xl relative z-10">
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Movies -->
    <section class="py-12 bg-gray-900">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-2xl font-bold">Filmes em Destaque</h2>
                <a href="#" class="text-pink-500 hover:text-pink-400 flex items-center">
                    Ver todos <i class="fas fa-chevron-right ml-1"></i>
                </a>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <!-- Movie Card 1 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTMxNTMwODM0NF5BMl5BanBnXkFtZTcwODAyMTk2Mw@@._V1_.jpg" alt="The Dark Knight" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">The Dark Knight</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">9.0</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-pink-600 text-xs px-2 py-1 rounded">Ação</span>
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                            <span class="genre-tag bg-purple-600 text-xs px-2 py-1 rounded">Crime</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Amigos
                        </button>
                    </div>
                </div>
                
                <!-- Movie Card 2 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMDFkYTc0MGEtZmNhMC00ZDIzLWFmNTEtODM1ZmRlYWMwMWFmXkEyXkFqcGdeQXVyMTMxODk2OTU@._V1_.jpg" alt="The Shawshank Redemption" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">The Shawshank Redemption</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">9.3</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Amigos
                        </button>
                    </div>
                </div>
                
                <!-- Movie Card 3 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMjAxMzY3NjcxNF5BMl5BanBnXkFtZTcwNTI5OTM0Mw@@._V1_.jpg" alt="Inception" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">Inception</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">8.8</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-pink-600 text-xs px-2 py-1 rounded">Ação</span>
                            <span class="genre-tag bg-purple-600 text-xs px-2 py-1 rounded">Ficção Científica</span>
                            <span class="genre-tag bg-indigo-600 text-xs px-2 py-1 rounded">Suspense</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Amigos
                        </button>
                    </div>
                </div>
                
                <!-- Movie Card 4 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMjE0NDk2NjgwOV5BMl5BanBnXkFtZTgwNTY0NTIwMjE@._V1_.jpg" alt="Your Name" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">Your Name</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">8.4</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-green-600 text-xs px-2 py-1 rounded">Animação</span>
                            <span class="genre-tag bg-teal-600 text-xs px-2 py-1 rounded">Fantasia</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Amigos
                        </button>
                    </div>
                </div>
                
                <!-- Movie Card 5 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTMxMjQ1MjA5Ml5BMl5BanBnXkFtZTcwNjIyNDc3OA@@._V1_.jpg" alt="The Avengers" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">The Avengers</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">8.0</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-pink-600 text-xs px-2 py-1 rounded">Ação</span>
                            <span class="genre-tag bg-purple-600 text-xs px-2 py-1 rounded">Ficção Científica</span>
                            <span class="genre-tag bg-yellow-600 text-xs px-2 py-1 rounded">Aventura</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Amigos
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Watch Together Feature -->
    <section class="py-16 bg-gray-800">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-4">Como assistir juntos no Kaua Gostoso</h2>
                <p class="text-xl max-w-3xl mx-auto">Conecte-se com quem você ama e compartilhe momentos especiais assistindo filmes juntos, mesmo à distância.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8">
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg text-center">
                    <div class="bg-pink-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-film text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">1. Escolha um filme</h3>
                    <p>Selecione entre milhares de filmes disponíveis gratuitamente em nossa plataforma.</p>
                </div>
                
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg text-center">
                    <div class="bg-yellow-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-user-friends text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">2. Convide amigos</h3>
                    <p>Compartilhe o link da sessão ou convide diretamente pelo nosso sistema.</p>
                </div>
                
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg text-center">
                    <div class="bg-green-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-play text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">3. Assista sincronizado</h3>
                    <p>Todos os participantes assistem juntos com áudio e vídeo sincronizados.</p>
                </div>
            </div>
            
            <div class="mt-12 text-center">
                <button class="bg-pink-600 hover:bg-pink-700 text-white px-8 py-3 rounded-full text-lg font-bold watch-party-btn">
                    <i class="fas fa-play-circle mr-2"></i> Criar Sessão Agora
                </button>
            </div>
        </div>
    </section>

    <!-- Romantic Movies Section -->
    <section class="py-12 bg-gray-900">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-2xl font-bold">Românticos para Assistir a Dois</h2>
                <a href="#" class="text-pink-500 hover:text-pink-400 flex items-center">
                    Ver todos <i class="fas fa-chevron-right ml-1"></i>
                </a>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <!-- Romantic Movie 1 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTk4OTI1NzYxOF5BMl5BanBnXkFtZTcwNjU1NTI0Mw@@._V1_.jpg" alt="The Notebook" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">The Notebook</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">7.8</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Namorada
                        </button>
                    </div>
                </div>
                
                <!-- Romantic Movie 2 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTQ4NjQ3NDg1Ml5BMl5BanBnXkFtZTcwNzI3Njg3OA@@._V1_.jpg" alt="La La Land" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">La La Land</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">8.0</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-yellow-600 text-xs px-2 py-1 rounded">Musical</span>
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Namorada
                        </button>
                    </div>
                </div>
                
                <!-- Romantic Movie 3 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTY5NzE3NzU3MF5BMl5BanBnXkFtZTgwMjg0NTQ5MDE@._V1_.jpg" alt="Little Women" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">Little Women</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">7.8</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                            <span class="genre-tag bg-purple-600 text-xs px-2 py-1 rounded">Histórico</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Namorada
                        </button>
                    </div>
                </div>
                
                <!-- Romantic Movie 4 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTk3NDE2NzI4NF5BMl5BanBnXkFtZTgwNzE1MzEyMTE@._V1_.jpg" alt="Crazy Rich Asians" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">Crazy Rich Asians</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">6.9</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-green-600 text-xs px-2 py-1 rounded">Comédia</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Namorada
                        </button>
                    </div>
                </div>
                
                <!-- Romantic Movie 5 -->
                <div class="movie-card relative rounded-lg overflow-hidden shadow-lg">
                    <img src="https://m.media-amazon.com/images/M/MV5BMTY0NjEwNDE3OV5BMl5BanBnXkFtZTgwNjA2MDE1MDE@._V1_.jpg" alt="About Time" class="w-full h-64 object-cover">
                    <div class="movie-overlay absolute inset-0 bg-gradient-to-t from-black to-transparent p-4 flex flex-col justify-end">
                        <h3 class="font-bold text-lg">About Time</h3>
                        <div class="flex items-center text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <span class="ml-1">7.8</span>
                        </div>
                        <div class="flex flex-wrap gap-1 mb-2">
                            <span class="genre-tag bg-red-600 text-xs px-2 py-1 rounded">Romance</span>
                            <span class="genre-tag bg-purple-600 text-xs px-2 py-1 rounded">Ficção Científica</span>
                            <span class="genre-tag bg-blue-600 text-xs px-2 py-1 rounded">Drama</span>
                        </div>
                        <button class="bg-pink-600 hover:bg-pink-700 text-white py-1 rounded watch-party-btn">
                            Assistir com Namorada
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="py-16 bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">O que dizem nossos usuários</h2>
            
            <div class="grid md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="User" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Ana Clara</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p>"Adorei assistir filmes românticos com meu namorado mesmo estando em cidades diferentes. O Kaua Gostoso tornou nosso relacionamento a distância mais especial!"</p>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="User" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Pedro Henrique</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p>"Finalmente um site com filmes grátis que realmente funciona! Assisto toda semana com meus amigos e a qualidade é excelente. Recomendo demais!"</p>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="bg-gray-700 p-6 rounded-lg shadow-lg">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="User" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Juliana</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p>"O sistema de assistir junto é incrível! Minha melhor amiga mudou de país e agora podemos continuar nosso ritual de assistir filmes toda sexta como antes."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Call to Action -->
    <section class="py-16 bg-gradient-to-r from-purple-900 to-pink-700">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6">Pronto para começar sua sessão de cinema virtual?</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">Junte-se a milhares de pessoas que já estão aproveitando filmes grátis com quem amam.</p>
            <button class="bg-white text-pink-600 px-8 py-3 rounded-full text-lg font-bold hover:bg-gray-100 transition watch-party-btn">
                <i class="fas fa-play-circle mr-2"></i> Criar Sessão Agora
            </button>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 py-12">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <i class="fas fa-film text-2xl text-pink-500"></i>
                        <h3 class="text-2xl font-bold bg-gradient-to-r from-pink-500 to-yellow-400 bg-clip-text text-transparent">Kaua Gostoso</h3>
                    </div>
                    <p class="text-gray-400">O melhor lugar para assistir filmes grátis com quem você ama.</p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-400 hover:text-pink-500"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-400 hover:text-pink-500"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-pink-500"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-400 hover:text-pink-500"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Links Rápidos</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Início</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Filmes</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Séries</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Assistir Juntos</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Sobre Nós</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Categorias</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Romance</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Ação</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Comédia</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Drama</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-500">Ficção Científica</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Newsletter</h4>
                    <p class="text-gray-400 mb-4">Inscreva-se para receber novidades e promoções.</p>
                    <div class="flex">
                        <input type="email" placeholder="Seu e-mail" class="bg-gray-800 text-white px-4 py-2 rounded-l focus:outline-none focus:ring-2 focus:ring-pink-500 w-full">
                        <button class="bg-pink-600 hover:bg-pink-700 px-4 rounded-r">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 mb-4 md:mb-0">© 2023 Kaua Gostoso. Todos os direitos reservados.</p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-pink-500">Termos de Serviço</a>
                    <a href="#" class="text-gray-400 hover:text-pink-500">Política de Privacidade</a>
                    <a href="#" class="text-gray-400 hover:text-pink-500">Contato</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript for mobile menu toggle
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('.md\\:hidden');
            const mobileMenu = document.querySelector('.md\\:flex');
            
            mobileMenuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
                mobileMenu.classList.toggle('flex');
                mobileMenu.classList.toggle('flex-col');
                mobileMenu.classList.toggle('absolute');
                mobileMenu.classList.toggle('top-16');
                mobileMenu.classList.toggle('left-0');
                mobileMenu.classList.toggle('right-0');
                mobileMenu.classList.toggle('bg-gray-800');
                mobileMenu.classList.toggle('p-4');
                mobileMenu.classList.toggle('space-y-4');
                mobileMenu.classList.toggle('space-x-6');
                mobileMenu.classList.toggle('shadow-lg');
            });
            
            // Smooth scroll for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
            
            // Watch party button animation
            const watchPartyButtons = document.querySelectorAll('.watch-party-btn');
            watchPartyButtons.forEach(button => {
                button.addEventListener('mouseenter', function() {
                    this.classList.add('transform', 'scale-105');
                });
                button.addEventListener('mouseleave', function() {
                    this.classList.remove('transform', 'scale-105');
                });
            });
        });
    </script>
</body>
</html>
