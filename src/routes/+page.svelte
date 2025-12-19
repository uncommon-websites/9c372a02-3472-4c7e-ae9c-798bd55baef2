<script lang="ts">
	import { onMount } from 'svelte';

	// Icons
	const ChevronRight = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>`;
	const ChevronLeft = `<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>`;
	const PlayCircle = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="10 8 16 12 10 16 10 8"/></svg>`;
	const Plus = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="M12 5v14"/></svg>`;
	const Check = `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"/></svg>`;
	const Instagram = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>`;
	const Linkedin = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>`;
	const XIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 6 6 18"/><path d="m6 6 18 18"/></svg>`;

	let faqs = [
		{ question: "What makes Stretch AI different from other stretching apps?", open: false },
		{ question: "Do I need any equipment to use Stretch AI?", open: false },
		{ question: "How long are the typical sessions?", open: false },
		{ question: "Is Stretch AI suitable for beginners?", open: false },
		{ question: "Can I use Stretch AI if I have an injury?", open: false }
	];

	function toggleFaq(index: number) {
		faqs = faqs.map((faq, i) => {
			if (i === index) return { ...faq, open: !faq.open };
			return faq;
		});
	}
</script>

<div class="min-h-screen flex flex-col font-sans text-white bg-black">
	<!-- Top Banner -->
	<div class="bg-white text-black text-[10px] font-bold py-3 text-center tracking-[0.15em] px-4 uppercase font-mono">
		<span class="text-[#FF0040]">◆</span> FIRST MONTH FREE — CODE: MOVE30 <span class="text-[#FF0040]">◆</span>
	</div>

	<!-- Navigation -->
	<nav class="flex items-center justify-between px-6 md:px-12 py-4 bg-black border-b-2 border-[#333333] relative">
		<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-[#00FF41] to-transparent opacity-50"></div>
		<div class="flex items-center gap-2">
			<!-- Logo -->
			<div class="flex items-center gap-3">
				<svg width="40" height="16" viewBox="0 0 1787 726" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M1059 726H0L195.537 531H1254.54L1059 726ZM1326.74 459H267.735L463.272 264H1522.27L1326.74 459ZM1591.46 195H532.463L728 0H1787L1591.46 195Z" fill="white"/>
				</svg>
				<span class="text-xl font-black tracking-tighter text-white uppercase">Stretch <span class="text-[#00FF41]">AI</span></span>
			</div>
		</div>
		<div class="hidden md:flex items-center gap-8 text-[11px] font-bold text-gray-400 uppercase tracking-wider">
			<a href="#" class="hover:text-[#00FF41] transition-colors">Programs</a>
			<a href="#" class="hover:text-[#00FF41] transition-colors">Science</a>
			<a href="#" class="hover:text-[#00FF41] transition-colors">Pricing</a>
			<a href="#" class="hover:text-[#00FF41] transition-colors">FAQ</a>
			<a href="#" class="bg-white text-black px-6 py-2.5 text-[11px] font-black hover:bg-[#00FF41] transition-all uppercase tracking-wider border-2 border-white hover:border-[#00FF41]">Start Trial</a>
		</div>
	</nav>

	<!-- Hero Section -->
	<section class="flex flex-col items-center pt-20 pb-24 px-4 text-center bg-black relative tech-grid-bg">
		<div class="absolute top-0 left-0 w-full h-full opacity-5 pointer-events-none">
			<div class="absolute top-20 left-10 w-32 h-32 border-2 border-[#00FF41]"></div>
			<div class="absolute top-40 right-20 w-24 h-24 border-2 border-[#00F0FF]"></div>
			<div class="absolute bottom-40 left-1/4 w-16 h-16 border-2 border-[#FF6B00]"></div>
		</div>
		
		<div class="mb-6 text-[10px] font-mono font-bold tracking-[0.2em] text-[#00FF41] uppercase">
			[ MOBILITY SYSTEM v2.0 ]
		</div>
		
		<h1 class="text-5xl md:text-[80px] leading-[0.95] font-black tracking-tighter max-w-4xl mb-8 text-white uppercase relative">
			Move better.<br>
			<span class="relative inline-block">
				Perform longer.
				<div class="absolute top-1/2 left-0 w-full h-[3px] bg-gradient-to-r from-transparent via-[#00FF41] to-transparent opacity-30"></div>
			</span>
		</h1>
		
		<div class="flex items-center gap-4 mb-8 text-[11px] font-mono font-bold text-gray-500 uppercase tracking-wider">
			<span class="flex items-center gap-2">
				<span class="w-2 h-2 bg-[#00FF41] animate-pulse"></span>
				Expert protocols
			</span>
			<span class="text-[#333333]">|</span>
			<span class="flex items-center gap-2">
				<span class="w-2 h-2 bg-[#00F0FF] animate-pulse"></span>
				Science-backed
			</span>
			<span class="text-[#333333]">|</span>
			<span class="flex items-center gap-2">
				<span class="w-2 h-2 bg-[#FF6B00] animate-pulse"></span>
				Proven results
			</span>
		</div>
		
		<p class="text-gray-400 text-[13px] max-w-2xl mb-10 leading-relaxed font-medium">
			Expert-led mobility and stretching programs designed for athletes, trainers, and anyone serious about longevity. Science-backed protocols that actually work.
		</p>
		
		<button class="bg-white text-black px-8 py-4 text-[11px] font-black hover:bg-[#00FF41] transition-all mb-24 uppercase tracking-[0.15em] border-2 border-white hover:border-[#00FF41] relative group">
			<span class="relative z-10">Start free trial</span>
			<div class="absolute inset-0 bg-[#00FF41] transform scale-x-0 group-hover:scale-x-100 transition-transform origin-left"></div>
		</button>

		<!-- Horizontal Scroll Images -->
		<div class="w-full max-w-[1400px] overflow-hidden relative">
			<div class="flex gap-6 justify-center items-center h-[320px]">
				<!-- Image 1 -->
				<div class="w-[200px] h-[260px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#00FF41] transition-colors">
					<img src="/generated/image-person-doing-a-deep-hip-flexor-stretch-o-1766105488969-0.webp" alt="Hip flexor stretch" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#00FF41] border border-[#00FF41]">HIP_01</div>
				</div>
				<!-- Image 2 -->
				<div class="w-[260px] h-[180px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#00F0FF] transition-colors -translate-y-2">
					<img src="/generated/image-athlete-performing-a-shoulder-mobility-e-1766105491074-1.webp" alt="Shoulder mobility" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#00F0FF] border border-[#00F0FF]">SHOULDER_02</div>
				</div>
				<!-- Image 3 -->
				<div class="w-[220px] h-[220px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#FF6B00] transition-colors translate-y-2">
					<img src="/generated/image-person-doing-a-hamstring-stretch-outdoor-1766105493131-2.webp" alt="Hamstring stretch" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#FF6B00] border border-[#FF6B00]">HAMSTRING_03</div>
				</div>
				<!-- Image 4 -->
				<div class="w-[200px] h-[200px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#00FF41] transition-colors -translate-y-4">
					<img src="/generated/image-runner-doing-a-quad-stretch-before-train-1766105495307-3.webp" alt="Quad stretch" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#00FF41] border border-[#00FF41]">QUAD_04</div>
				</div>
				<!-- Image 5 -->
				<div class="w-[180px] h-[260px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#00F0FF] transition-colors translate-y-6">
					<img src="/generated/image-person-doing-a-spinal-twist-stretch-on-t-1766105497640-4.webp" alt="Spinal twist" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#00F0FF] border border-[#00F0FF]">SPINE_05</div>
				</div>
				<!-- Image 6 -->
				<div class="w-[200px] h-[160px] overflow-hidden flex-shrink-0 relative group border-2 border-[#1F1F1F] hover:border-[#FF6B00] transition-colors -translate-y-2">
					<img src="/generated/image-athlete-performing-foam-rolling-for-reco-1766105499649-5.webp" alt="Foam rolling recovery" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all" />
					<div class="absolute top-2 left-2 bg-black/80 px-2 py-1 text-[8px] font-mono font-bold text-[#FF6B00] border border-[#FF6B00]">RECOVERY_06</div>
				</div>
			</div>
		</div>
	</section>

	<!-- App Showcase -->
	<section class="py-24 px-6 md:px-12 flex justify-center bg-black relative">
		<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-12 md:p-20 flex flex-col md:flex-row items-center gap-16 max-w-[1200px] w-full relative overflow-hidden">
			<!-- Technical corner accents -->
			<div class="absolute top-0 left-0 w-20 h-20 border-t-2 border-l-2 border-[#00FF41] opacity-30"></div>
			<div class="absolute bottom-0 right-0 w-20 h-20 border-b-2 border-r-2 border-[#00F0FF] opacity-30"></div>
			
			<!-- Phone Mockup -->
			<div class="relative w-[280px] h-[580px] bg-black p-3 flex-shrink-0 border-2 border-[#333333]">
				<div class="w-full h-full bg-white overflow-hidden relative">
					<!-- Fake App UI -->
					<div class="p-6 pt-10">
						<div class="flex justify-between items-center mb-6">
							<div class="text-[10px] font-black uppercase tracking-wider">Today's Session</div>
							<div class="w-6 h-6 bg-black border-2 border-black"></div>
						</div>
						<div class="bg-black p-4 mb-4 text-white border-2 border-black relative overflow-hidden">
							<div class="absolute top-0 right-0 w-16 h-16 border-2 border-[#00FF41] opacity-20"></div>
							<div class="text-[8px] font-mono font-bold mb-1 text-[#00FF41]">MOBILITY_PROTOCOL</div>
							<div class="text-base font-black mb-2 uppercase">Hip Flexor Series</div>
							<div class="text-[8px] font-mono opacity-80">15:00 • INTERMEDIATE</div>
						</div>
						<div class="space-y-3">
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 bg-[#00FF41] flex items-center justify-center text-[10px] font-black text-black border-2 border-[#00FF41]">✓</div>
								<div class="flex-1">
									<div class="text-[9px] font-bold uppercase">Warm-up Flow</div>
									<div class="h-1.5 bg-[#00FF41] w-full mt-1"></div>
								</div>
							</div>
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 border-2 border-black flex items-center justify-center text-[10px] font-black">2</div>
								<div class="flex-1">
									<div class="text-[9px] font-bold uppercase">Hip Flexor Stretch</div>
									<div class="h-1.5 bg-gray-200 w-full mt-1"></div>
								</div>
							</div>
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 border-2 border-gray-200 flex items-center justify-center text-[10px] font-bold text-gray-400">3</div>
								<div class="flex-1">
									<div class="text-[9px] font-bold uppercase text-gray-400">Cool Down</div>
									<div class="h-1.5 bg-gray-200 w-full mt-1"></div>
								</div>
							</div>
						</div>
					</div>
					<!-- Bottom Nav -->
					<div class="absolute bottom-0 left-0 w-full h-16 bg-white border-t-2 border-black flex justify-around items-center px-4">
						<div class="w-6 h-6 bg-black"></div>
						<div class="w-6 h-6 border-2 border-gray-300"></div>
						<div class="w-6 h-6 border-2 border-gray-300"></div>
						<div class="w-6 h-6 border-2 border-gray-300"></div>
					</div>
				</div>
			</div>

			<!-- Content -->
			<div class="flex-1 max-w-lg">
				<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#00F0FF] uppercase mb-4">
					[ INTELLIGENT TRACKING ]
				</div>
				<h2 class="text-3xl font-black mb-6 leading-tight text-white uppercase tracking-tight">
					Your mobility journey, simplified.
				</h2>
				<p class="text-gray-400 text-[13px] leading-relaxed mb-8">
					Follow expert-designed protocols, track your progress, and see measurable improvements in range of motion. Every session is structured, scientifically-backed, and built to help you move better for life.
				</p>
				
				<!-- Technical stats -->
				<div class="grid grid-cols-3 gap-4 mb-8 pb-8 border-b-2 border-[#1F1F1F]">
					<div>
						<div class="text-2xl font-black text-[#00FF41] font-mono">98%</div>
						<div class="text-[9px] font-bold text-gray-500 uppercase tracking-wider">Completion</div>
					</div>
					<div>
						<div class="text-2xl font-black text-[#00F0FF] font-mono">15m</div>
						<div class="text-[9px] font-bold text-gray-500 uppercase tracking-wider">Avg Session</div>
					</div>
					<div>
						<div class="text-2xl font-black text-[#FF6B00] font-mono">+24%</div>
						<div class="text-[9px] font-bold text-gray-500 uppercase tracking-wider">ROM Gain</div>
					</div>
				</div>
				
				<div class="flex items-center justify-between">
					<a href="#" class="flex items-center gap-2 text-[#00FF41] text-[11px] font-bold hover:text-white transition-colors uppercase tracking-wider">
						{@html PlayCircle}
						Watch demo
					</a>
					<div class="flex gap-4">
						<button class="w-10 h-10 flex items-center justify-center border-2 border-[#333333] hover:border-[#00FF41] hover:bg-[#00FF41] hover:text-black transition-all">
							{@html ChevronLeft}
						</button>
						<button class="w-10 h-10 flex items-center justify-center border-2 border-[#333333] hover:border-[#00FF41] hover:bg-[#00FF41] hover:text-black transition-all">
							{@html ChevronRight}
						</button>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Lifestyle Grid -->
	<section class="py-20 px-6 md:px-12 max-w-[1400px] mx-auto w-full bg-black">
		<div class="flex flex-col md:flex-row justify-between items-start mb-16 gap-10">
			<div>
				<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#FF6B00] uppercase mb-4">
					[ PERFORMANCE SYSTEM ]
				</div>
				<h2 class="text-4xl md:text-5xl font-black tracking-tighter max-w-md leading-[0.95] text-white uppercase">
					Built for those who take performance seriously.
				</h2>
			</div>
			<p class="text-gray-400 text-[13px] max-w-md leading-relaxed">
				Whether you're an athlete, trainer, or fitness enthusiast, mobility is the foundation of longevity. Stretch AI gives you the structure, expertise, and consistency you need to move better, prevent injury, and perform at your peak.
			</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<!-- Card 1 -->
			<div class="relative h-[480px] overflow-hidden group border-2 border-[#1F1F1F] hover:border-[#00FF41] transition-colors">
				<img src="/generated/image-confident-female-athlete-in-her-30s-doin-1766105501646-6.webp" alt="Structured mobility routine" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700" />
				<div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent flex flex-col justify-end p-8 text-white">
					<div class="text-[8px] font-mono font-bold text-[#00FF41] mb-3 tracking-[0.2em]">PROTOCOL_01</div>
					<h3 class="text-2xl font-black mb-2 uppercase">Expert-led protocols.</h3>
					<p class="text-[12px] text-white/80 leading-relaxed">No guesswork. Follow structured programs designed by sports scientists and physical therapists.</p>
				</div>
				<!-- Corner accent -->
				<div class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-[#00FF41] opacity-0 group-hover:opacity-100 transition-opacity"></div>
			</div>
			<!-- Card 2 -->
			<div class="relative h-[480px] overflow-hidden group border-2 border-[#1F1F1F] hover:border-[#00F0FF] transition-colors">
				<img src="/generated/image-male-athlete-tracking-progress-on-his-ph-1766105503901-7.webp" alt="Tracking progress" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700" />
				<div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent flex flex-col justify-end p-8 text-white">
					<div class="text-[8px] font-mono font-bold text-[#00F0FF] mb-3 tracking-[0.2em]">TRACKING_02</div>
					<h3 class="text-2xl font-black mb-2 uppercase">Track real progress.</h3>
					<p class="text-[12px] text-white/80 leading-relaxed">Measure improvements in range of motion and see how consistency transforms your mobility.</p>
				</div>
				<!-- Corner accent -->
				<div class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-[#00F0FF] opacity-0 group-hover:opacity-100 transition-opacity"></div>
			</div>
			<!-- Card 3 -->
			<div class="relative h-[480px] overflow-hidden group border-2 border-[#1F1F1F] hover:border-[#FF6B00] transition-colors">
				<img src="/generated/image-person-doing-recovery-stretches-in-a-pea-1766105506054-8.webp" alt="Recovery and longevity" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700" />
				<div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent flex flex-col justify-end p-8 text-white">
					<div class="text-[8px] font-mono font-bold text-[#FF6B00] mb-3 tracking-[0.2em]">LONGEVITY_03</div>
					<h3 class="text-2xl font-black mb-2 uppercase">Prevent injury. Extend your career.</h3>
					<p class="text-[12px] text-white/80 leading-relaxed">Mobility work isn't optional—it's essential for longevity and peak performance.</p>
				</div>
				<!-- Corner accent -->
				<div class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-[#FF6B00] opacity-0 group-hover:opacity-100 transition-opacity"></div>
			</div>
		</div>
	</section>

	<!-- Testimonial -->
	<section class="py-24 px-6 text-center bg-[#0A0A0A] border-y-2 border-[#1F1F1F] relative overflow-hidden">
		<!-- Technical grid background -->
		<div class="absolute inset-0 tech-grid-bg opacity-30"></div>
		
		<!-- Corner accents -->
		<div class="absolute top-0 left-0 w-32 h-32 border-t-2 border-l-2 border-[#00FF41] opacity-20"></div>
		<div class="absolute bottom-0 right-0 w-32 h-32 border-b-2 border-r-2 border-[#00F0FF] opacity-20"></div>
		
		<div class="max-w-3xl mx-auto relative z-10">
			<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#00FF41] uppercase mb-8">
				[ EXPERT VALIDATION ]
			</div>
			
			<blockquote class="text-2xl md:text-3xl font-black leading-tight mb-10 text-white uppercase tracking-tight">
				"Stretch AI is what I've been recommending to my athletes for years—structured, evidence-based mobility work that actually delivers results."
			</blockquote>
			
			<div class="flex flex-col items-center gap-4">
				<img src="/generated/image-professional-physical-therapist-or-sport-1766105508492-9.webp" alt="Physical Therapist" class="w-16 h-16 object-cover border-2 border-[#00FF41] grayscale" />
				<div class="text-sm">
					<div class="font-black text-white uppercase tracking-wide">Dr. Marcus Chen, DPT</div>
					<div class="text-[11px] text-gray-400 font-mono">SPORTS_PHYSICAL_THERAPIST</div>
				</div>
			</div>
			
			<!-- Verification badge -->
			<div class="mt-8 inline-flex items-center gap-2 px-4 py-2 border-2 border-[#00FF41] text-[9px] font-mono font-bold text-[#00FF41] uppercase tracking-wider">
				<span class="w-2 h-2 bg-[#00FF41] animate-pulse"></span>
				Verified Professional
			</div>
		</div>
	</section>

	<!-- Process Steps -->
	<section class="py-20 px-6 md:px-12 max-w-[1400px] mx-auto w-full border-b-2 border-[#1F1F1F] bg-black">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
			<div class="border-l-2 border-[#00FF41] pl-6 relative">
				<div class="absolute -left-[9px] top-0 w-4 h-4 bg-[#00FF41] border-2 border-black"></div>
				<div class="text-[10px] font-mono font-bold text-[#00FF41] mb-3 tracking-[0.2em]">STEP_01</div>
				<h3 class="text-xl font-black mb-3 text-white uppercase">Sign up in 2 minutes.</h3>
				<p class="text-[12px] text-gray-400 leading-relaxed">Create your account, answer a few questions about your goals, and get instant access to all programs.</p>
				<div class="mt-4 text-[10px] font-mono text-gray-600">TIME: 00:02:00</div>
			</div>
			<div class="border-l-2 border-[#00F0FF] pl-6 relative">
				<div class="absolute -left-[9px] top-0 w-4 h-4 bg-[#00F0FF] border-2 border-black"></div>
				<div class="text-[10px] font-mono font-bold text-[#00F0FF] mb-3 tracking-[0.2em]">STEP_02</div>
				<h3 class="text-xl font-black mb-3 text-white uppercase">Start your first session.</h3>
				<p class="text-[12px] text-gray-400 leading-relaxed">Follow expert-guided protocols designed for your level. Each session is clear, structured, and effective.</p>
				<div class="mt-4 text-[10px] font-mono text-gray-600">TIME: 00:15:00</div>
			</div>
			<div class="border-l-2 border-[#FF6B00] pl-6 relative">
				<div class="absolute -left-[9px] top-0 w-4 h-4 bg-[#FF6B00] border-2 border-black"></div>
				<div class="text-[10px] font-mono font-bold text-[#FF6B00] mb-3 tracking-[0.2em]">STEP_03</div>
				<h3 class="text-xl font-black mb-3 text-white uppercase">Track your progress.</h3>
				<p class="text-[12px] text-gray-400 leading-relaxed">See measurable improvements in mobility and range of motion. Build consistency that lasts.</p>
				<div class="mt-4 text-[10px] font-mono text-gray-600">ONGOING</div>
			</div>
		</div>
	</section>

	<!-- How it works -->
	<section class="py-24 px-6 md:px-12 max-w-[1400px] mx-auto w-full bg-black">
		<div class="flex flex-col lg:flex-row gap-20">
			<!-- Sticky Title -->
			<div class="lg:w-1/3 lg:sticky lg:top-24 h-fit">
				<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#00FF41] uppercase mb-4">
					[ SYSTEM OVERVIEW ]
				</div>
				<h2 class="text-4xl font-black mb-6 text-white uppercase tracking-tight">How it works.</h2>
				<p class="text-gray-400 text-[13px] leading-relaxed max-w-xs mb-8">
					Stretch AI combines expert-designed protocols with intelligent tracking to deliver a complete mobility system. No guesswork, no generic routines—just proven methods that help you move better.
				</p>
				
				<!-- Technical stats sidebar -->
				<div class="border-2 border-[#1F1F1F] p-4 space-y-3">
					<div class="flex justify-between items-center pb-2 border-b border-[#1F1F1F]">
						<span class="text-[9px] font-mono text-gray-500 uppercase">Active Users</span>
						<span class="text-sm font-black font-mono text-[#00FF41]">12.4K</span>
					</div>
					<div class="flex justify-between items-center pb-2 border-b border-[#1F1F1F]">
						<span class="text-[9px] font-mono text-gray-500 uppercase">Protocols</span>
						<span class="text-sm font-black font-mono text-[#00F0FF]">150+</span>
					</div>
					<div class="flex justify-between items-center">
						<span class="text-[9px] font-mono text-gray-500 uppercase">Avg Improvement</span>
						<span class="text-sm font-black font-mono text-[#FF6B00]">+28%</span>
					</div>
				</div>
			</div>

			<!-- Steps List -->
			<div class="lg:w-2/3 flex flex-col gap-8">
				<!-- Step 1 -->
				<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-16 flex flex-col items-center text-center relative overflow-hidden">
					<div class="absolute top-0 left-0 w-24 h-24 border-t-2 border-l-2 border-[#00FF41] opacity-20"></div>
					<div class="w-full max-w-md mb-10 text-left self-start relative z-10">
						<div class="w-10 h-10 border-2 border-[#00FF41] flex items-center justify-center text-sm font-black mb-6 text-[#00FF41] font-mono">01</div>
						<h3 class="text-2xl font-black mb-3 text-white uppercase">Choose your program.</h3>
						<p class="text-[12px] text-gray-400 leading-relaxed">Select from targeted programs for different goals—whether you're focused on recovery, performance, or injury prevention. All programs are designed by experts.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black p-2 border-2 border-[#333333]">
						<div class="w-full h-full bg-white overflow-hidden relative flex flex-col">
                            <!-- Mock UI -->
                            <div class="bg-black p-4 border-b-2 border-black">
                                <div class="h-3 w-20 bg-white mb-2"></div>
                            </div>
                            <div class="p-4 space-y-3">
                                <div class="h-12 bg-black border-2 border-black p-2">
                                    <div class="h-2 w-16 bg-[#00FF41] mb-1"></div>
                                    <div class="h-3 w-28 bg-white"></div>
                                </div>
                                <div class="h-12 bg-white border-2 border-gray-200 p-2">
                                    <div class="h-2 w-16 bg-gray-200 mb-1"></div>
                                    <div class="h-3 w-28 bg-gray-300"></div>
                                </div>
                                <div class="h-12 bg-white border-2 border-gray-200 p-2">
                                    <div class="h-2 w-16 bg-gray-200 mb-1"></div>
                                    <div class="h-3 w-28 bg-gray-300"></div>
                                </div>
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 2 -->
				<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-16 flex flex-col items-center text-center relative overflow-hidden">
					<div class="absolute top-0 right-0 w-24 h-24 border-t-2 border-r-2 border-[#00F0FF] opacity-20"></div>
					<div class="w-full max-w-md mb-10 text-left self-start relative z-10">
						<div class="w-10 h-10 border-2 border-[#00F0FF] flex items-center justify-center text-sm font-black mb-6 text-[#00F0FF] font-mono">02</div>
						<h3 class="text-2xl font-black mb-3 text-white uppercase">Follow guided sessions.</h3>
						<p class="text-[12px] text-gray-400 leading-relaxed">Each session provides clear video instruction and real-time guidance. Know exactly what to do, how long to hold, and when to progress.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black p-2 border-2 border-[#333333]">
                        <div class="w-full h-full bg-white overflow-hidden relative flex flex-col items-center pt-8">
                            <div class="text-[10px] font-black mb-4 uppercase tracking-wider">Today's Session</div>
                            <div class="w-32 h-32 bg-black border-2 border-black mb-4 flex items-center justify-center">
                                <div class="w-0 h-0 border-l-[20px] border-l-white border-t-[15px] border-t-transparent border-b-[15px] border-b-transparent ml-1"></div>
                            </div>
                            <div class="text-[10px] font-black px-8 text-center uppercase">Hip Mobility Protocol</div>
                            <div class="text-[9px] font-mono text-gray-400 px-8 text-center mt-1">15:00 MINUTES</div>
                            <div class="mt-auto w-full p-4">
                                <div class="w-full h-10 bg-black border-2 border-black"></div>
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 3 -->
				<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-16 flex flex-col items-center text-center relative overflow-hidden">
					<div class="absolute bottom-0 left-0 w-24 h-24 border-b-2 border-l-2 border-[#FF6B00] opacity-20"></div>
					<div class="w-full max-w-md mb-10 text-left self-start relative z-10">
						<div class="w-10 h-10 border-2 border-[#FF6B00] flex items-center justify-center text-sm font-black mb-6 text-[#FF6B00] font-mono">03</div>
						<h3 class="text-2xl font-black mb-3 text-white uppercase">Track your improvements.</h3>
						<p class="text-[12px] text-gray-400 leading-relaxed">See measurable progress in range of motion and mobility scores. The platform tracks your consistency and shows how you're improving over time.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black p-2 border-2 border-[#333333]">
                        <div class="w-full h-full bg-black overflow-hidden relative text-white p-6 pt-10 border-2 border-[#1F1F1F]">
                             <div class="flex items-center gap-3 mb-6 pb-4 border-b-2 border-[#1F1F1F]">
                                 <div class="w-10 h-10 border-2 border-[#00FF41]"></div>
                                 <div>
                                     <div class="text-[10px] font-black uppercase">Your Progress</div>
                                     <div class="text-[8px] font-mono text-gray-400">WEEK_04</div>
                                 </div>
                             </div>
                             <div class="space-y-3">
                                 <div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-3">
                                     <div class="text-[8px] font-mono text-gray-400 mb-2">HIP_MOBILITY</div>
                                     <div class="flex items-center gap-2">
                                         <div class="flex-1 h-2 bg-[#1F1F1F] overflow-hidden">
                                             <div class="h-full bg-[#00FF41] w-3/4"></div>
                                         </div>
                                         <div class="text-[10px] font-black font-mono text-[#00FF41]">+12%</div>
                                     </div>
                                 </div>
                                 <div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-3">
                                     <div class="text-[8px] font-mono text-gray-400 mb-2">SHOULDER_ROM</div>
                                     <div class="flex items-center gap-2">
                                         <div class="flex-1 h-2 bg-[#1F1F1F] overflow-hidden">
                                             <div class="h-full bg-[#00F0FF] w-2/3"></div>
                                         </div>
                                         <div class="text-[10px] font-black font-mono text-[#00F0FF]">+8%</div>
                                     </div>
                                 </div>
                             </div>
                        </div>
					</div>
				</div>

				<!-- Step 4 -->
				<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-16 flex flex-col items-center text-center relative overflow-hidden">
					<div class="absolute top-0 right-0 w-24 h-24 border-t-2 border-r-2 border-[#00FF41] opacity-20"></div>
					<div class="w-full max-w-md mb-10 text-left self-start relative z-10">
						<div class="w-10 h-10 border-2 border-[#00FF41] flex items-center justify-center text-sm font-black mb-6 text-[#00FF41] font-mono">04</div>
						<h3 class="text-2xl font-black mb-3 text-white uppercase">Get personalized insights.</h3>
						<p class="text-[12px] text-gray-400 leading-relaxed">Receive expert guidance on areas to focus on, modifications for your body, and recommendations to accelerate your progress.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black p-2 border-2 border-[#333333]">
                        <div class="w-full h-full bg-white overflow-hidden relative flex flex-col pt-8 px-4">
                            <div class="text-center text-[10px] font-black mb-4 uppercase tracking-wider">AI Insights</div>
                            <div class="text-[9px] text-black leading-relaxed text-left space-y-3">
                                <div class="border-l-2 border-[#00FF41] pl-2">
                                    <div class="font-black mb-1">HIP MOBILITY +12%</div>
                                    <div class="text-gray-600">Your hip mobility has improved significantly over the past 3 weeks. Consider adding the Advanced Hip Protocol.</div>
                                </div>
                                <div class="border-l-2 border-[#FF6B00] pl-2">
                                    <div class="font-black mb-1">ASYMMETRY DETECTED</div>
                                    <div class="text-gray-600">Your shoulder range of motion shows asymmetry. Focus on the Shoulder Stability series.</div>
                                </div>
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 5 -->
				<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-16 flex flex-col items-center text-center relative overflow-hidden">
					<div class="absolute bottom-0 right-0 w-24 h-24 border-b-2 border-r-2 border-[#00F0FF] opacity-20"></div>
					<div class="w-full max-w-md mb-10 text-left self-start relative z-10">
						<div class="w-10 h-10 border-2 border-[#00F0FF] flex items-center justify-center text-sm font-black mb-6 text-[#00F0FF] font-mono">05</div>
						<h3 class="text-2xl font-black mb-3 text-white uppercase">Build lasting habits.</h3>
						<p class="text-[12px] text-gray-400 leading-relaxed">Consistency is key. The platform helps you build a sustainable mobility practice that becomes part of your routine, not another thing to stress about.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black p-2 border-2 border-[#333333]">
                        <div class="w-full h-full bg-white overflow-hidden relative flex flex-col pt-8 px-4">
                             <div class="bg-black border-2 border-black p-3 text-[9px] mb-3 text-white font-black uppercase">
                                 Why is consistency more important than intensity?
                             </div>
                             <div class="text-[9px] text-black leading-relaxed mt-2">
                                 Mobility improvements come from regular, progressive work—not occasional intense sessions. Your nervous system adapts through repetition and consistency...
                             </div>
                             
                             <!-- Streak indicator -->
                             <div class="mt-auto mb-4 border-2 border-black p-3">
                                 <div class="text-[8px] font-mono text-gray-500 mb-2">CURRENT STREAK</div>
                                 <div class="text-2xl font-black font-mono">28 DAYS</div>
                             </div>
                        </div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Dark Cards Section -->
	<section class="py-10 px-6 md:px-12 max-w-[1400px] mx-auto w-full bg-black">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			<!-- Left Card -->
			<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-12 text-white min-h-[400px] flex flex-col relative overflow-hidden">
				<div class="absolute top-0 left-0 w-24 h-24 border-t-2 border-l-2 border-[#00FF41] opacity-20"></div>
				<div class="relative z-10">
					<div class="text-[10px] font-mono font-bold text-[#00FF41] mb-3 tracking-[0.2em]">EVIDENCE_BASED</div>
					<h3 class="text-2xl font-black max-w-xs uppercase leading-tight">Designed by sports scientists and physical therapists.</h3>
				</div>
				<!-- Data visualization -->
				<div class="absolute bottom-8 right-8 w-48 h-48 opacity-10">
					<div class="grid grid-cols-4 gap-2 h-full items-end">
						<div class="bg-[#00FF41] h-1/2"></div>
						<div class="bg-[#00FF41] h-3/4"></div>
						<div class="bg-[#00FF41] h-full"></div>
						<div class="bg-[#00FF41] h-2/3"></div>
					</div>
				</div>
				<!-- Technical readout -->
				<div class="mt-auto relative z-10">
					<div class="border-t-2 border-[#1F1F1F] pt-4 font-mono text-[10px] text-gray-600">
						<div class="flex justify-between mb-1">
							<span>PROTOCOLS</span>
							<span class="text-[#00FF41]">150+</span>
						</div>
						<div class="flex justify-between">
							<span>VALIDATION</span>
							<span class="text-[#00FF41]">PEER_REVIEWED</span>
						</div>
					</div>
				</div>
			</div>
			<!-- Right Card -->
			<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-10 md:p-12 text-white min-h-[400px] flex flex-col relative overflow-hidden">
				<div class="absolute top-0 right-0 w-24 h-24 border-t-2 border-r-2 border-[#00F0FF] opacity-20"></div>
				<div class="relative z-10">
					<div class="text-[10px] font-mono font-bold text-[#00F0FF] mb-3 tracking-[0.2em]">SECURITY_FIRST</div>
					<h3 class="text-2xl font-black max-w-xs uppercase leading-tight">Privacy-first platform built for professionals.</h3>
				</div>
				<!-- Encrypted data visual -->
				<div class="absolute bottom-8 right-8 text-right font-mono text-2xl opacity-10 select-none pointer-events-none">
					<div class="text-[#00F0FF]">████████</div>
					<div class="text-[#00F0FF]">██████</div>
					<div class="text-[#00F0FF]">███████████</div>
					<div class="text-[#00F0FF]">█████</div>
				</div>
				<!-- Technical readout -->
				<div class="mt-auto relative z-10">
					<div class="border-t-2 border-[#1F1F1F] pt-4 font-mono text-[10px] text-gray-600">
						<div class="flex justify-between mb-1">
							<span>ENCRYPTION</span>
							<span class="text-[#00F0FF]">AES_256</span>
						</div>
						<div class="flex justify-between">
							<span>COMPLIANCE</span>
							<span class="text-[#00F0FF]">HIPAA_READY</span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Pricing Section -->
	<section class="py-24 px-6 md:px-12 max-w-[1400px] mx-auto w-full text-center bg-black">
		<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#FF6B00] uppercase mb-4">
			[ PRICING ]
		</div>
		<h2 class="text-3xl md:text-4xl font-black mb-4 text-white uppercase">Invest in your mobility.</h2>
		<p class="text-gray-400 text-[13px] max-w-lg mx-auto mb-16">
			Expert-designed programs, intelligent tracking, and personalized guidance—all in one platform. Choose the plan that fits your goals.
		</p>

		<div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-4xl mx-auto">
			<!-- Monthly Plan -->
			<div class="bg-[#0A0A0A] border-2 border-[#1F1F1F] p-8 text-left flex flex-col relative overflow-hidden">
				<div class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-[#1F1F1F] opacity-50"></div>
				<div class="w-10 h-10 border-2 border-[#333333] mb-6"></div>
				<h3 class="text-xl font-black mb-1 text-white uppercase">Monthly</h3>
				<p class="text-[10px] font-mono text-gray-400 mb-6 uppercase tracking-wider">Try it out, cancel anytime.</p>
				
				<div class="flex items-baseline gap-2 mb-1">
					<span class="text-3xl font-black text-white font-mono">$29</span>
					<span class="text-[10px] font-mono text-gray-500">/MONTH</span>
				</div>
				<div class="text-[9px] font-mono text-[#00FF41] mb-8">CODE: MOVE30 → FIRST_MONTH_FREE</div>

				<ul class="space-y-4 mb-8 flex-1">
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Access to all mobility and stretching programs
					</li>
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Progress tracking and mobility assessments
					</li>
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Expert video instruction for every movement
					</li>
				</ul>

				<button class="w-full bg-white text-black py-3 text-[11px] font-black hover:bg-[#00FF41] transition-all uppercase tracking-wider border-2 border-white hover:border-[#00FF41]">Start Trial</button>
			</div>

			<!-- Annual Plan -->
			<div class="bg-[#0A0A0A] border-2 border-[#00FF41] p-8 text-left flex flex-col relative overflow-hidden">
                <div class="absolute top-0 right-0 bg-[#00FF41] text-black text-[9px] font-black px-3 py-1.5 font-mono tracking-wider">BEST_VALUE</div>
				<div class="absolute top-0 left-0 w-16 h-16 border-t-2 border-l-2 border-[#00FF41] opacity-30"></div>
				<div class="w-10 h-10 bg-[#00FF41] border-2 border-[#00FF41] mb-6"></div>
				<h3 class="text-xl font-black mb-1 text-white uppercase">Annual</h3>
				<p class="text-[10px] font-mono text-gray-400 mb-6 uppercase tracking-wider">Save 40% with annual billing.</p>
				
				<div class="flex items-baseline gap-2 mb-1">
					<span class="text-3xl font-black text-white font-mono">$199</span>
					<span class="text-[10px] font-mono text-gray-500">/YEAR</span>
				</div>
				<div class="text-[9px] font-mono text-[#00FF41] mb-8">$16.58/MONTH → SAVE $149 ANNUALLY</div>

				<ul class="space-y-4 mb-8 flex-1">
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Everything in Monthly, plus priority support
					</li>
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Early access to new programs and features
					</li>
					<li class="flex gap-3 text-[11px] text-gray-400">
						<span class="text-[#00FF41] shrink-0 font-black">{@html Check}</span>
						Personalized program recommendations and insights
					</li>
				</ul>

				<button class="w-full bg-[#00FF41] text-black py-3 text-[11px] font-black hover:bg-white transition-all uppercase tracking-wider border-2 border-[#00FF41] hover:border-white">Start Trial</button>
			</div>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-20 px-6 md:px-12 max-w-3xl mx-auto w-full bg-black">
		<div class="text-[10px] font-mono font-bold tracking-[0.2em] text-[#00F0FF] uppercase mb-4 text-center">
			[ SUPPORT ]
		</div>
		<h2 class="text-3xl font-black text-center mb-16 text-white uppercase">Your questions answered.</h2>
		<div class="space-y-4">
			{#each faqs as faq, i}
				<button 
					class="w-full flex items-center justify-between p-5 text-left hover:bg-[#0A0A0A] transition-colors group border-2 border-[#1F1F1F] hover:border-[#00FF41] relative"
					onclick={() => toggleFaq(i)}
				>
					<div class="flex items-start gap-4 flex-1">
						<span class="text-[10px] font-mono font-black text-gray-600 mt-0.5">Q{i + 1}</span>
						<span class="text-[13px] font-bold text-white uppercase tracking-tight">{faq.question}</span>
					</div>
					<span class="text-[#00FF41] transition-transform duration-200 {faq.open ? 'rotate-45' : ''} ml-4">{@html Plus}</span>
				</button>
                {#if faq.open}
                    <div class="px-5 pb-5 pt-2 text-[12px] text-gray-400 leading-relaxed border-l-2 border-[#00FF41] ml-5 pl-8">
                        {#if i === 0}
                            Stretch AI combines expert-designed protocols with intelligent tracking and personalized guidance. Unlike generic stretching apps, our programs are created by sports scientists and physical therapists, backed by research, and structured to deliver measurable results.
                        {:else if i === 1}
                            Most programs require no equipment at all. Some advanced protocols may use optional tools like resistance bands or foam rollers, but these are never required to get started.
                        {:else if i === 2}
                            Sessions range from 10-30 minutes depending on the program. We believe in consistency over intensity—short, focused sessions that fit into your routine are more effective than occasional long workouts.
                        {:else if i === 3}
                            Absolutely. Every program includes modifications for different experience levels. Our guided instruction ensures you understand proper form and progression, making it safe and effective for beginners.
                        {:else if i === 4}
                            While our programs are designed to prevent injury and support recovery, we always recommend consulting with your healthcare provider before starting any new movement program if you have an existing injury.
                        {/if}
                    </div>
                {/if}
			{/each}
		</div>
		<div class="text-center mt-12">
			<button class="bg-[#0A0A0A] border-2 border-[#333333] px-8 py-3 text-[11px] font-black hover:bg-[#1F1F1F] hover:border-[#00FF41] transition-all text-white uppercase tracking-wider">
				View all FAQs
			</button>
		</div>
	</section>

	<!-- Footer -->
	<footer class="bg-[#0A0A0A] border-t-2 border-[#1F1F1F] py-16 px-6 md:px-12 text-[10px] text-gray-500 relative overflow-hidden">
		<div class="absolute top-0 left-0 w-full h-[1px] bg-gradient-to-r from-transparent via-[#00FF41] to-transparent opacity-30"></div>
		
		<div class="max-w-[1400px] mx-auto">
			<div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-12 gap-8 pb-8 border-b-2 border-[#1F1F1F]">
				<div class="flex items-center gap-3">
					<svg width="40" height="16" viewBox="0 0 1787 726" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M1059 726H0L195.537 531H1254.54L1059 726ZM1326.74 459H267.735L463.272 264H1522.27L1326.74 459ZM1591.46 195H532.463L728 0H1787L1591.46 195Z" fill="white"/>
					</svg>
					<span class="text-lg font-black tracking-tighter text-white uppercase">Stretch <span class="text-[#00FF41]">AI</span></span>
				</div>
				<div class="flex flex-wrap gap-6 font-bold text-gray-500 uppercase tracking-wider">
					<a href="#" class="hover:text-[#00FF41] transition-colors">Programs</a>
					<a href="#" class="hover:text-[#00FF41] transition-colors">Science</a>
					<a href="#" class="hover:text-[#00FF41] transition-colors">Pricing</a>
					<a href="#" class="hover:text-[#00FF41] transition-colors">FAQ</a>
					<a href="#" class="hover:text-[#00FF41] transition-colors">Terms</a>
					<a href="#" class="hover:text-[#00FF41] transition-colors">Privacy</a>
				</div>
				<div class="flex gap-4">
					<a href="#" class="text-gray-400 hover:text-[#00FF41] transition-colors border-2 border-[#1F1F1F] hover:border-[#00FF41] p-2">{@html XIcon}</a>
					<a href="#" class="text-gray-400 hover:text-[#00FF41] transition-colors border-2 border-[#1F1F1F] hover:border-[#00FF41] p-2">{@html Instagram}</a>
					<a href="#" class="text-gray-400 hover:text-[#00FF41] transition-colors border-2 border-[#1F1F1F] hover:border-[#00FF41] p-2">{@html Linkedin}</a>
				</div>
			</div>
			
			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
				<div>
					<div class="text-[9px] font-mono font-bold text-gray-600 mb-3 tracking-[0.2em]">LEGAL_DISCLAIMER</div>
					<p class="text-[11px] leading-relaxed text-gray-500">Stretch AI is a digital platform providing mobility and stretching guidance. Our programs are designed by qualified professionals but do not constitute medical advice, diagnosis, or treatment.</p>
				</div>
				<div>
					<div class="text-[9px] font-mono font-bold text-gray-600 mb-3 tracking-[0.2em]">RESULTS_DISCLAIMER</div>
					<p class="text-[11px] leading-relaxed text-gray-500">Results may vary based on individual commitment, consistency, and physical condition. The testimonials and progress examples shown represent individual experiences.</p>
				</div>
				<div>
					<div class="text-[9px] font-mono font-bold text-gray-600 mb-3 tracking-[0.2em]">SUBSCRIPTION_TERMS</div>
					<p class="text-[11px] leading-relaxed text-gray-500">By subscribing, you agree to our Terms & Conditions and Privacy Policy. You can cancel your subscription at any time. Message and data rates may apply.</p>
				</div>
			</div>
			
			<div class="text-center pt-8 border-t-2 border-[#1F1F1F]">
				<div class="text-[9px] font-mono text-gray-600">
					© 2024 STRETCH_AI • ALL_RIGHTS_RESERVED • v2.0.1
				</div>
			</div>
		</div>
	</footer>
</div>

<style>
    /* Hide scrollbar for horizontal scroll */
    .overflow-hidden::-webkit-scrollbar {
        display: none;
    }
</style>

