import React, { useState, useEffect } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Globe, Calendar, Clock, MapPin, Navigation, Gift, Star, Sparkles } from "lucide-react";
import { motion } from "framer-motion";

export default function InvitationPage() {
  const [language, setLanguage] = useState('he');
  const [mounted, setMounted] = useState(false);

  useEffect(() => {
    setMounted(true);
  }, []);

  const content = {
    he: {
      title: "מזל טוב – חוגגים 50!",
      subtitle: "הזמנה מיוחדת לחגיגה בלתי נשכחת",
      inviteText: "נשמח לראותכם בחגיגה גדולה לכבוד יום הולדת 50.",
      eventDetails: "פרטי האירוע",
      date: "תאריך:",
      dateValue: "יום חמישי, 1 בינואר 2026",
      time: "שעה:",
      timeValue: "20:00",
      location: "מיקום:",
      locationValue: "אולם אירועים \"שם האולם\"",
      navigationBtn: "לחצו כאן לניווט",
      footerText: "מצפים לראותכם!",
      googleMaps: "Google Maps",
      waze: "Waze",
      changeLanguage: "English"
    },
    en: {
      title: "Happy 50th Birthday!",
      subtitle: "Special Invitation to an Unforgettable Celebration",
      inviteText: "We would love to see you at a grand celebration for a 50th birthday.",
      eventDetails: "Event Details",
      date: "Date:",
      dateValue: "Thursday, January 1, 2026",
      time: "Time:",
      timeValue: "8:00 PM",
      location: "Location:",
      locationValue: "Event Hall \"Hall Name\"",
      navigationBtn: "Click Here for Navigation",
      footerText: "Looking forward to seeing you!",
      googleMaps: "Google Maps", 
      waze: "Waze",
      changeLanguage: "עברית"
    }
  };

  const currentContent = content[language];
  const isRTL = language === 'he';

  const handleNavigation = (service) => {
    const address = "אולם אירועים שם האולם"; // Replace with actual address
    if (service === 'google') {
      window.open(`https://maps.google.com/maps?q=${encodeURIComponent(address)}`, '_blank');
    } else if (service === 'waze') {
      window.open(`https://waze.com/ul?q=${encodeURIComponent(address)}`, '_blank');
    }
  };

  if (!mounted) {
    return <div className="min-h-screen bg-gradient-to-br from-amber-50 to-yellow-100"></div>;
  }

  return (
    <div dir={isRTL ? "rtl" : "ltr"} className="min-h-screen bg-gradient-to-br from-amber-50 via-orange-50 to-yellow-100 relative overflow-hidden">
      {/* Decorative Background Elements */}
      <div className="absolute inset-0 overflow-hidden">
        <div className="absolute top-10 left-10 w-20 h-20 bg-gradient-to-r from-amber-400 to-yellow-400 rounded-full opacity-20 animate-pulse"></div>
        <div className="absolute top-40 right-16 w-16 h-16 bg-gradient-to-r from-orange-400 to-amber-400 rounded-full opacity-20 animate-bounce" style={{animationDelay: '1s'}}></div>
        <div className="absolute bottom-20 left-20 w-12 h-12 bg-gradient-to-r from-yellow-400 to-orange-400 rounded-full opacity-20 animate-pulse" style={{animationDelay: '2s'}}></div>
        <div className="absolute bottom-40 right-10 w-24 h-24 bg-gradient-to-r from-amber-400 to-yellow-400 rounded-full opacity-15 animate-bounce" style={{animationDelay: '0.5s'}}></div>
        
        {/* Floating Sparkles */}
        <div className="absolute top-32 left-1/4">
          <Sparkles className="w-6 h-6 text-amber-400 opacity-60 animate-pulse" />
        </div>
        <div className="absolute bottom-32 right-1/3">
          <Star className="w-5 h-5 text-yellow-400 opacity-60 animate-pulse" style={{animationDelay: '1.5s'}} />
        </div>
        <div className="absolute top-1/2 left-12">
          <Gift className="w-7 h-7 text-orange-400 opacity-50 animate-bounce" style={{animationDelay: '2.5s'}} />
        </div>
      </div>

      {/* Language Toggle */}
      <motion.div 
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
        className="absolute top-6 right-6 z-10"
      >
        <Button
          variant="ghost"
          onClick={() => setLanguage(language === 'he' ? 'en' : 'he')}
          className="bg-white/80 backdrop-blur-sm hover:bg-white/90 border border-amber-200 text-gray-700 font-medium rounded-full px-4 py-2 shadow-lg transition-all duration-300"
        >
          <Globe className="w-4 h-4 mr-2" />
          {currentContent.changeLanguage}
        </Button>
      </motion.div>

      <div className="relative z-10 container mx-auto px-4 py-12 min-h-screen flex items-center justify-center">
        <motion.div 
          initial={{ opacity: 0, scale: 0.9 }}
          animate={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.8, ease: "easeOut" }}
          className="w-full max-w-4xl"
        >
          {/* Main Invitation Card */}
          <Card className="backdrop-blur-lg bg-white/90 shadow-2xl border-0 overflow-hidden rounded-3xl">
            <CardContent className="p-8 md:p-12 text-center">
              
              {/* Header Section */}
              <motion.div 
                initial={{ opacity: 0, y: 30 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.3, duration: 0.7 }}
                className="mb-8"
              >
                <div className="relative inline-block mb-4">
                  <h1 className="text-4xl md:text-6xl font-bold bg-gradient-to-r from-amber-600 via-yellow-500 to-orange-500 bg-clip-text text-transparent mb-4 leading-tight">
                    {currentContent.title}
                  </h1>
                  <div className="absolute -top-4 -right-4 text-3xl animate-bounce">🎉</div>
                  <div className="absolute -bottom-2 -left-4 text-2xl animate-pulse">✨</div>
                </div>
                
                <motion.p 
                  initial={{ opacity: 0 }}
                  animate={{ opacity: 1 }}
                  transition={{ delay: 0.6 }}
                  className="text-lg md:text-xl text-gray-600 font-medium mb-8"
                >
                  {currentContent.subtitle}
                </motion.p>
              </motion.div>

              {/* Image Section */}
              <motion.div 
                initial={{ opacity: 0, scale: 0.8 }}
                animate={{ opacity: 1, scale: 1 }}
                transition={{ delay: 0.4, duration: 0.7 }}
                className="mb-8"
              >
                <div className="relative mx-auto w-full max-w-md h-64 bg-gradient-to-br from-amber-100 to-yellow-200 rounded-2xl shadow-lg flex items-center justify-center overflow-hidden border-4 border-amber-200">
                  <img 
                    src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?w=400&h=250&fit=crop&crop=center" 
                    alt="Birthday celebration"
                    className="w-full h-full object-cover"
                  />
                  <div className="absolute inset-0 bg-gradient-to-t from-amber-900/20 to-transparent"></div>
                  <div className="absolute bottom-4 left-1/2 transform -translate-x-1/2">
                    <div className="bg-white/90 backdrop-blur-sm px-4 py-2 rounded-full shadow-lg">
                      <span className="text-amber-800 font-semibold text-sm">🎂 50 שנים מדהימות!</span>
                    </div>
                  </div>
                </div>
              </motion.div>

              {/* Invitation Text */}
              <motion.div 
                initial={{ opacity: 0, y: 20 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.5, duration: 0.7 }}
                className="mb-10"
              >
                <p className="text-lg md:text-xl text-gray-700 leading-relaxed font-medium">
                  {currentContent.inviteText}
                </p>
              </motion.div>

              {/* Event Details */}
              <motion.div 
                initial={{ opacity: 0, y: 30 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.6, duration: 0.7 }}
                className="mb-10"
              >
                <div className="bg-gradient-to-r from-amber-50 to-yellow-50 rounded-2xl p-6 md:p-8 shadow-inner border border-amber-200/50">
                  <h2 className="text-2xl md:text-3xl font-bold text-amber-800 mb-6 flex items-center justify-center gap-3">
                    <Star className="w-7 h-7 text-amber-500" />
                    {currentContent.eventDetails}
                    <Star className="w-7 h-7 text-amber-500" />
                  </h2>
                  
                  <div className="grid md:grid-cols-3 gap-6 text-center">
                    <div className="space-y-3">
                      <div className="w-16 h-16 mx-auto bg-gradient-to-r from-amber-400 to-yellow-400 rounded-full flex items-center justify-center shadow-lg">
                        <Calendar className="w-8 h-8 text-white" />
                      </div>
                      <div>
                        <p className="text-sm font-semibold text-amber-800 uppercase tracking-wide mb-1">{currentContent.date}</p>
                        <p className="text-lg font-bold text-gray-800">{currentContent.dateValue}</p>
                      </div>
                    </div>

                    <div className="space-y-3">
                      <div className="w-16 h-16 mx-auto bg-gradient-to-r from-orange-400 to-amber-400 rounded-full flex items-center justify-center shadow-lg">
                        <Clock className="w-8 h-8 text-white" />
                      </div>
                      <div>
                        <p className="text-sm font-semibold text-amber-800 uppercase tracking-wide mb-1">{currentContent.time}</p>
                        <p className="text-lg font-bold text-gray-800">{currentContent.timeValue}</p>
                      </div>
                    </div>

                    <div className="space-y-3">
                      <div className="w-16 h-16 mx-auto bg-gradient-to-r from-yellow-400 to-orange-400 rounded-full flex items-center justify-center shadow-lg">
                        <MapPin className="w-8 h-8 text-white" />
                      </div>
                      <div>
                        <p className="text-sm font-semibold text-amber-800 uppercase tracking-wide mb-1">{currentContent.location}</p>
                        <p className="text-lg font-bold text-gray-800">{currentContent.locationValue}</p>
                      </div>
                    </div>
                  </div>
                </div>
              </motion.div>

              {/* Navigation Buttons */}
              <motion.div 
                initial={{ opacity: 0, y: 20 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.7, duration: 0.7 }}
                className="mb-10"
              >
                <h3 className="text-xl font-bold text-gray-800 mb-4 flex items-center justify-center gap-2">
                  <Navigation className="w-5 h-5 text-amber-600" />
                  {currentContent.navigationBtn}
                </h3>
                
                <div className="flex flex-col sm:flex-row gap-4 justify-center">
                  <Button
                    onClick={() => handleNavigation('google')}
                    className="bg-gradient-to-r from-blue-500 to-blue-600 hover:from-blue-600 hover:to-blue-700 text-white px-8 py-3 rounded-full font-semibold shadow-lg transform hover:scale-105 transition-all duration-300 flex items-center gap-3"
                  >
                    <img src="https://developers.google.com/maps/images/google_maps_platform_logo.svg" alt="Google Maps" className="w-5 h-5" />
                    {currentContent.googleMaps}
                  </Button>
                  
                  <Button
                    onClick={() => handleNavigation('waze')}
                    className="bg-gradient-to-r from-cyan-500 to-blue-500 hover:from-cyan-600 hover:to-blue-600 text-white px-8 py-3 rounded-full font-semibold shadow-lg transform hover:scale-105 transition-all duration-300 flex items-center gap-3"
                  >
                    🚗
                    {currentContent.waze}
                  </Button>
                </div>
              </motion.div>

              {/* Decorative Elements */}
              <motion.div 
                initial={{ opacity: 0 }}
                animate={{ opacity: 1 }}
                transition={{ delay: 0.8, duration: 1 }}
                className="flex justify-center items-center gap-8 mb-8"
              >
                <div className="text-6xl animate-bounce" style={{animationDelay: '0s'}}>🎈</div>
                <div className="text-5xl animate-bounce" style={{animationDelay: '0.2s'}}>🎊</div>
                <div className="text-6xl animate-bounce" style={{animationDelay: '0.4s'}}>🎉</div>
                <div className="text-5xl animate-bounce" style={{animationDelay: '0.6s'}}>🎈</div>
              </motion.div>

              {/* Footer */}
              <motion.div 
                initial={{ opacity: 0, y: 20 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.9, duration: 0.7 }}
                className="pt-8 border-t border-amber-200"
              >
                <p className="text-2xl font-bold bg-gradient-to-r from-amber-600 to-orange-500 bg-clip-text text-transparent">
                  {currentContent.footerText}
                </p>
                <div className="flex justify-center items-center gap-2 mt-4">
                  <div className="text-2xl animate-pulse">💖</div>
                  <div className="text-2xl animate-pulse" style={{animationDelay: '0.5s'}}>✨</div>
                  <div className="text-2xl animate-pulse" style={{animationDelay: '1s'}}>🌟</div>
                </div>
              </motion.div>

            </CardContent>
          </Card>
        </motion.div>
      </div>

      {/* Floating Confetti Animation */}
      <div className="absolute inset-0 pointer-events-none">
        {[...Array(12)].map((_, i) => (
          <motion.div
            key={i}
            className="absolute text-2xl"
            style={{
              left: `${10 + (i * 7)}%`,
              top: `-10%`,
            }}
            animate={{
              y: ['0vh', '110vh'],
              rotate: [0, 360],
              opacity: [0, 1, 1, 0]
            }}
            transition={{
              duration: 8 + (i % 3),
              repeat: Infinity,
              delay: i * 0.5,
              ease: "linear"
            }}
          >
            {['🎊', '✨', '🎉', '⭐'][i % 4]}
          </motion.div>
        ))}
      </div>

      {/* Custom Styles */}
      <style jsx>{`
        @import url('https://fonts.googleapis.com/css2?family=Assistant:wght@300;400;600;700;800&display=swap');
        
        * {
          font-family: 'Assistant', system-ui, -apple-system, sans-serif;
        }

        .animate-float {
          animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
          0%, 100% { transform: translateY(0px); }
          50% { transform: translateY(-10px); }
        }

        .text-shadow-gold {
          text-shadow: 2px 2px 8px rgba(251, 191, 36, 0.3);
        }

        body {
          overflow-x: hidden;
        }
      `}</style>
    </div>
  );
}