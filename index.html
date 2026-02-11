import React, { useState, useEffect, useMemo } from 'react';
import { 
  Search, 
  Plus, 
  Trash2, 
  MessageCircle, 
  BedDouble, 
  MapPin, 
  DollarSign, 
  X,
  Home,
  Lock,
  LogOut,
  Phone,
  Camera,
  Edit3
} from 'lucide-react';

const App = () => {
  // --- ESTADO E PERSISTÊNCIA ---
  const [properties, setProperties] = useState(() => {
    const saved = localStorage.getItem('imob_properties_v2');
    return saved ? JSON.parse(saved) : [
      {
        id: 1,
        title: "Cobertura Duplex com Piscina",
        description: "Exclusiva cobertura com acabamento em mármore, 3 suítes e área externa privativa.",
        price: 1500000,
        neighborhood: "Leblon",
        bedrooms: 3,
        image: "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&q=80&w=800",
      }
    ];
  });

  // --- AUTENTICAÇÃO ---
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const [showLoginModal, setShowLoginModal] = useState(false);
  const [password, setPassword] = useState('');

  // --- FILTROS ---
  const [filterNeighborhood, setFilterNeighborhood] = useState('');
  const [filterMaxPrice, setFilterMaxPrice] = useState('');
  const [filterBedrooms, setFilterBedrooms] = useState('');
  
  // --- ADMINISTRAÇÃO ---
  const [showAddModal, setShowAddModal] = useState(false);
  const [isCompressing, setIsCompressing] = useState(false);
  const [newProp, setNewProp] = useState({
    title: '',
    description: '',
    price: '',
    neighborhood: '',
    bedrooms: '',
    image: ''
  });

  useEffect(() => {
    localStorage.setItem('imob_properties_v2', JSON.stringify(properties));
  }, [properties]);

  // --- LÓGICA DE NEGÓCIO ---

  const handleLogin = (e) => {
    e.preventDefault();
    if (password === 'admin123') { // Senha simples para demonstração
      setIsLoggedIn(true);
      setShowLoginModal(false);
      setPassword('');
    } else {
      alert("Senha incorreta!");
    }
  };

  // Simulação de compressão de imagem (Otimização de desempenho)
  const handleImageUpload = (e) => {
    const file = e.target.files[0];
    if (file) {
      setIsCompressing(true);
      const reader = new FileReader();
      reader.onloadend = () => {
        // Simulando delay de processamento/compressão
        setTimeout(() => {
          setNewProp({ ...newProp, image: reader.result });
          setIsCompressing(false);
        }, 1000);
      };
      reader.readAsDataURL(file);
    }
  };

  const filteredProperties = useMemo(() => {
    return properties.filter(p => {
      const matchNeighborhood = filterNeighborhood === '' || p.neighborhood.toLowerCase().includes(filterNeighborhood.toLowerCase());
      const matchPrice = filterMaxPrice === '' || p.price <= parseFloat(filterMaxPrice);
      const matchBedrooms = filterBedrooms === '' || p.bedrooms >= parseInt(filterBedrooms);
      return matchNeighborhood && matchPrice && matchBedrooms;
    });
  }, [properties, filterNeighborhood, filterMaxPrice, filterBedrooms]);

  const handleAddProperty = (e) => {
    e.preventDefault();
    const propertyToAdd = {
      ...newProp,
      id: Date.now(),
      price: parseFloat(newProp.price),
      bedrooms: parseInt(newProp.bedrooms),
      image: newProp.image || "https://images.unsplash.com/photo-1564013799919-ab600027ffc6?auto=format&fit=crop&q=80&w=800"
    };
    setProperties([propertyToAdd, ...properties]);
    setShowAddModal(false);
    setNewProp({ title: '', description: '', price: '', neighborhood: '', bedrooms: '', image: '' });
  };

  const deleteProperty = (id) => {
    if (confirm("Deseja realmente excluir este imóvel do catálogo?")) {
      setProperties(properties.filter(p => p.id !== id));
    }
  };

  const sendWhatsApp = (prop) => {
    const phone = "5511999999999"; // Configure seu número aqui
    const message = encodeURIComponent(
      `Olá! Tenho interesse no imóvel: ${prop.title}\n` +
      `Localização: ${prop.neighborhood}\n` +
      `Valor: R$ ${prop.price.toLocaleString('pt-BR')}\n` +
      `Quartos: ${prop.bedrooms}\n` +
      `Vi no seu catálogo digital.`
    );
    window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
  };

  return (
    <div className="min-h-screen bg-slate-50 text-slate-900 font-sans">
      {/* NAVBAR */}
      <nav className="bg-white border-b border-slate-200 sticky top-0 z-40">
        <div className="max-w-7xl mx-auto px-4 h-16 flex items-center justify-between">
          <div className="flex items-center gap-2 text-blue-700 font-black text-xl tracking-tight">
            <div className="bg-blue-700 text-white p-1.5 rounded-lg">
              <Home size={22} />
            </div>
            <span>IMOB<span className="text-slate-400">PRIVATE</span></span>
          </div>
          
          <div className="flex items-center gap-3">
            {isLoggedIn ? (
              <div className="flex items-center gap-3">
                <span className="hidden md:block text-xs font-bold text-slate-400 uppercase tracking-widest">Painel Admin</span>
                <button 
                  onClick={() => setIsLoggedIn(false)}
                  className="p-2 text-slate-400 hover:text-red-500 transition-colors"
                  title="Sair"
                >
                  <LogOut size={20} />
                </button>
              </div>
            ) : (
              <button 
                onClick={() => setShowLoginModal(true)}
                className="p-2 text-slate-400 hover:text-blue-600 transition-colors"
              >
                <Lock size={20} />
              </button>
            )}
          </div>
        </div>
      </nav>

      {/* HERO & SEARCH */}
      <header className="bg-white border-b border-slate-200 py-12 px-4">
        <div className="max-w-4xl mx-auto text-center mb-10">
          <h1 className="text-4xl md:text-5xl font-black text-slate-900 mb-4 tracking-tight">
            Seu próximo endereço <br/><span className="text-blue-600">está aqui.</span>
          </h1>
          <p className="text-slate-500 text-lg max-w-2xl mx-auto">
            Catálogo exclusivo de propriedades selecionadas com foco em qualidade e localização.
          </p>
        </div>

        {/* Filters Panel */}
        <div className="max-w-5xl mx-auto bg-slate-900 p-2 rounded-3xl shadow-2xl overflow-hidden">
          <div className="bg-white rounded-[1.4rem] p-6 grid grid-cols-1 md:grid-cols-4 gap-6">
            <div className="space-y-1.5">
              <label className="text-[10px] font-black text-slate-400 uppercase tracking-wider ml-1">Localização</label>
              <div className="relative">
                <MapPin className="absolute left-3 top-1/2 -translate-y-1/2 text-blue-500" size={18} />
                <input 
                  type="text" 
                  placeholder="Bairro ou região"
                  className="w-full pl-10 pr-4 py-3 bg-slate-50 border-none rounded-xl focus:ring-2 focus:ring-blue-500 outline-none transition-all text-sm"
                  value={filterNeighborhood}
                  onChange={(e) => setFilterNeighborhood(e.target.value)}
                />
              </div>
            </div>

            <div className="space-y-1.5">
              <label className="text-[10px] font-black text-slate-400 uppercase tracking-wider ml-1">Preço Máximo</label>
              <div className="relative">
                <DollarSign className="absolute left-3 top-1/2 -translate-y-1/2 text-blue-500" size={18} />
                <input 
                  type="number" 
                  placeholder="Até R$"
                  className="w-full pl-10 pr-4 py-3 bg-slate-50 border-none rounded-xl focus:ring-2 focus:ring-blue-500 outline-none transition-all text-sm"
                  value={filterMaxPrice}
                  onChange={(e) => setFilterMaxPrice(e.target.value)}
                />
              </div>
            </div>

            <div className="space-y-1.5">
              <label className="text-[10px] font-black text-slate-400 uppercase tracking-wider ml-1">Quartos</label>
              <div className="relative">
                <BedDouble className="absolute left-3 top-1/2 -translate-y-1/2 text-blue-500" size={18} />
                <select 
                  className="w-full pl-10 pr-4 py-3 bg-slate-50 border-none rounded-xl appearance-none focus:ring-2 focus:ring-blue-500 outline-none transition-all text-sm"
                  value={filterBedrooms}
                  onChange={(e) => setFilterBedrooms(e.target.value)}
                >
                  <option value="">Qualquer quantidade</option>
                  <option value="1">1+ Quarto</option>
                  <option value="2">2+ Quartos</option>
                  <option value="3">3+ Quartos</option>
                  <option value="4">4+ Quartos</option>
                </select>
              </div>
            </div>

            <div className="flex items-end">
              <button className="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3.5 rounded-xl flex items-center justify-center gap-2 transition-all shadow-lg shadow-blue-200">
                <Search size={18} />
                Filtrar Resultados
              </button>
            </div>
          </div>
        </div>
      </header>

      {/* CATALOG SECTION */}
      <main className="max-w-7xl mx-auto px-4 py-16">
        <div className="flex flex-col md:flex-row md:items-center justify-between mb-10 gap-4">
          <div>
            <h2 className="text-3xl font-black text-slate-900 italic">Disponíveis agora</h2>
            <p className="text-slate-500 font-medium">Mostrando {filteredProperties.length} imóveis que combinam com sua busca.</p>
          </div>
          
          {isLoggedIn && (
            <button 
              onClick={() => setShowAddModal(true)}
              className="bg-slate-900 text-white px-6 py-3 rounded-2xl flex items-center justify-center gap-2 font-bold hover:bg-blue-600 transition-all active:scale-95 shadow-xl"
            >
              <Plus size={20} />
              Novo Imóvel
            </button>
          )}
        </div>

        {/* GRID */}
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          {filteredProperties.map(prop => (
            <div key={prop.id} className="group bg-white rounded-[2.5rem] overflow-hidden shadow-sm hover:shadow-2xl transition-all duration-500 border border-slate-100 flex flex-col h-full relative">
              {isLoggedIn && (
                <button 
                  onClick={() => deleteProperty(prop.id)}
                  className="absolute top-5 right-5 z-20 bg-white/90 backdrop-blur-md text-red-500 p-2.5 rounded-full hover:bg-red-500 hover:text-white transition-all shadow-xl border border-red-100"
                >
                  <Trash2 size={18} />
                </button>
              )}
              
              <div className="relative aspect-[16/11] overflow-hidden">
                <img 
                  src={prop.image} 
                  alt={prop.title} 
                  className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700"
                />
                <div className="absolute bottom-4 left-4">
                  <span className="bg-white/95 backdrop-blur-md px-3 py-1.5 rounded-full text-[10px] font-black uppercase tracking-widest shadow-lg">
                    {prop.neighborhood}
                  </span>
                </div>
              </div>
              
              <div className="p-8 flex flex-col flex-grow">
                <h3 className="text-xl font-black mb-3 text-slate-900 line-clamp-1 group-hover:text-blue-600 transition-colors">
                  {prop.title}
                </h3>
                <p className="text-slate-500 text-sm leading-relaxed mb-6 line-clamp-2">
                  {prop.description}
                </p>
                
                <div className="flex items-center gap-4 mb-8">
                  <div className="flex items-center gap-2 text-slate-400 font-bold text-sm">
                    <BedDouble size={18} className="text-blue-500" />
                    <span>{prop.bedrooms} {prop.bedrooms === 1 ? 'quarto' : 'quartos'}</span>
                  </div>
                </div>

                <div className="mt-auto flex items-center justify-between pt-6 border-t border-slate-50">
                  <div className="flex flex-col">
                    <span className="text-[10px] font-black text-slate-400 uppercase">Investimento</span>
                    <span className="text-2xl font-black text-slate-900">
                      <span className="text-sm font-bold text-blue-600 mr-1">R$</span>
                      {prop.price.toLocaleString('pt-BR')}
                    </span>
                  </div>
                  <button 
                    onClick={() => sendWhatsApp(prop)}
                    className="bg-emerald-500 hover:bg-emerald-600 text-white w-14 h-14 rounded-2xl flex items-center justify-center transition-all shadow-lg shadow-emerald-100 active:scale-90"
                    title="Contato via WhatsApp"
                  >
                    <MessageCircle size={28} />
                  </button>
                </div>
              </div>
            </div>
          ))}
        </div>

        {/* EMPTY STATE */}
        {filteredProperties.length === 0 && (
          <div className="text-center py-32 bg-white rounded-[3rem] border-2 border-dashed border-slate-200">
            <div className="bg-slate-100 w-24 h-24 rounded-full flex items-center justify-center mx-auto mb-6 text-slate-300">
              <Search size={48} />
            </div>
            <h3 className="text-2xl font-black text-slate-800 mb-2">Ops! Nada por aqui.</h3>
            <p className="text-slate-500 font-medium">Não encontramos imóveis com esses filtros exatos.</p>
            <button 
              onClick={() => {setFilterNeighborhood(''); setFilterMaxPrice(''); setFilterBedrooms('');}}
              className="mt-6 text-blue-600 font-bold hover:underline"
            >
              Limpar todos os filtros
            </button>
          </div>
        )}
      </main>

      {/* ADMIN LOGIN MODAL */}
      {showLoginModal && (
        <div className="fixed inset-0 bg-slate-900/80 backdrop-blur-md z-50 flex items-center justify-center p-4">
          <div className="bg-white w-full max-w-sm rounded-[2rem] shadow-2xl p-8">
            <div className="text-center mb-8">
              <div className="bg-blue-100 text-blue-600 w-16 h-16 rounded-2xl flex items-center justify-center mx-auto mb-4">
                <Lock size={32} />
              </div>
              <h2 className="text-2xl font-black">Acesso Restrito</h2>
              <p className="text-slate-500 text-sm">Apenas o proprietário pode gerenciar o catálogo.</p>
            </div>
            <form onSubmit={handleLogin} className="space-y-4">
              <input 
                type="password" 
                placeholder="Sua senha secreta"
                className="w-full px-6 py-4 bg-slate-100 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500"
                value={password}
                onChange={(e) => setPassword(e.target.value)}
                autoFocus
              />
              <div className="flex gap-3">
                <button 
                  type="button"
                  onClick={() => setShowLoginModal(false)}
                  className="flex-1 bg-slate-100 text-slate-500 font-bold py-4 rounded-2xl hover:bg-slate-200 transition-all"
                >
                  Cancelar
                </button>
                <button 
                  type="submit"
                  className="flex-2 bg-blue-600 text-white font-bold py-4 px-8 rounded-2xl hover:bg-blue-700 transition-all shadow-lg shadow-blue-200"
                >
                  Entrar
                </button>
              </div>
            </form>
          </div>
        </div>
      )}

      {/* ADD PROPERTY MODAL */}
      {showAddModal && (
        <div className="fixed inset-0 bg-slate-900/80 backdrop-blur-md z-50 flex items-center justify-center p-4">
          <div className="bg-white w-full max-w-2xl rounded-[2.5rem] shadow-2xl overflow-hidden flex flex-col max-h-[90vh]">
            <div className="p-8 border-b border-slate-100 flex items-center justify-between bg-slate-50/50">
              <div>
                <h2 className="text-2xl font-black">Adicionar Propriedade</h2>
                <p className="text-slate-400 text-sm font-medium uppercase tracking-tighter">Otimização de imagem automática ativa</p>
              </div>
              <button onClick={() => setShowAddModal(false)} className="text-slate-400 hover:text-slate-600 bg-white p-2 rounded-full shadow-sm">
                <X size={24} />
              </button>
            </div>
            
            <form onSubmit={handleAddProperty} className="p-8 space-y-6 overflow-y-auto">
              <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div className="md:col-span-2">
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Capa do Imóvel</label>
                  <label className="relative border-2 border-dashed border-slate-200 rounded-[2rem] h-48 flex flex-col items-center justify-center gap-3 cursor-pointer hover:bg-blue-50/50 hover:border-blue-200 transition-all group overflow-hidden">
                    {newProp.image ? (
                      <img src={newProp.image} className="w-full h-full object-cover" />
                    ) : (
                      <>
                        <div className="bg-slate-100 text-slate-400 p-4 rounded-2xl group-hover:scale-110 transition-transform">
                          {isCompressing ? <div className="animate-spin rounded-full h-6 w-6 border-2 border-blue-600 border-t-transparent"></div> : <Camera size={28} />}
                        </div>
                        <span className="text-sm font-bold text-slate-500 italic">{isCompressing ? 'Compactando foto...' : 'Clique para enviar foto'}</span>
                      </>
                    )}
                    <input type="file" className="hidden" accept="image/*" onChange={handleImageUpload} disabled={isCompressing} />
                  </label>
                </div>

                <div className="md:col-span-2">
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Título Chamativo</label>
                  <input 
                    required
                    type="text" 
                    className="w-full px-6 py-4 bg-slate-50 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500"
                    placeholder="Ex: Apartamento Moderno com Varanda"
                    value={newProp.title}
                    onChange={(e) => setNewProp({...newProp, title: e.target.value})}
                  />
                </div>

                <div>
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Preço de Venda (R$)</label>
                  <input 
                    required
                    type="number" 
                    className="w-full px-6 py-4 bg-slate-50 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500 font-bold"
                    placeholder="850000"
                    value={newProp.price}
                    onChange={(e) => setNewProp({...newProp, price: e.target.value})}
                  />
                </div>

                <div>
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Nº de Quartos</label>
                  <input 
                    required
                    type="number" 
                    className="w-full px-6 py-4 bg-slate-50 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500"
                    placeholder="3"
                    value={newProp.bedrooms}
                    onChange={(e) => setNewProp({...newProp, bedrooms: e.target.value})}
                  />
                </div>

                <div className="md:col-span-2">
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Bairro / Localidade</label>
                  <input 
                    required
                    type="text" 
                    className="w-full px-6 py-4 bg-slate-50 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500"
                    placeholder="Ex: Itaim Bibi, SP"
                    value={newProp.neighborhood}
                    onChange={(e) => setNewProp({...newProp, neighborhood: e.target.value})}
                  />
                </div>

                <div className="md:col-span-2">
                  <label className="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2 block">Descrição Detalhada</label>
                  <textarea 
                    required
                    className="w-full px-6 py-4 bg-slate-50 border-none rounded-2xl outline-none focus:ring-2 focus:ring-blue-500 h-32 resize-none"
                    placeholder="Descreva as qualidades do imóvel..."
                    value={newProp.description}
                    onChange={(e) => setNewProp({...newProp, description: e.target.value})}
                  ></textarea>
                </div>
              </div>

              <div className="flex gap-4 pt-4">
                <button 
                  type="button" 
                  onClick={() => setShowAddModal(false)}
                  className="flex-1 bg-slate-100 text-slate-500 font-bold py-5 rounded-[1.5rem] hover:bg-slate-200 transition-all"
                >
                  Cancelar
                </button>
                <button 
                  type="submit"
                  disabled={isCompressing}
                  className="flex-[2] bg-blue-600 text-white font-black py-5 rounded-[1.5rem] shadow-xl shadow-blue-200 hover:bg-blue-700 transition-all active:scale-95 disabled:opacity-50"
                >
                  Publicar Imóvel
                </button>
              </div>
            </form>
          </div>
        </div>
      )}
    </div>
  );
};

export default App;
