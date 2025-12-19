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

<div class="min-h-screen flex flex-col font-sans text-gray-900 bg-[#FAFAFA]">
	<!-- Top Banner -->
	<div class="bg-black text-white text-[11px] font-medium py-3 text-center tracking-wide px-4">
		Start your mobility journey today — First month free with code MOVE30
	</div>

	<!-- Navigation -->
	<nav class="flex items-center justify-between px-6 md:px-12 py-5 bg-[#FAFAFA]">
		<div class="flex items-center gap-2">
			<!-- Logo -->
			<div class="flex items-center gap-3">
				<svg width="40" height="16" viewBox="0 0 1787 726" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M1059 726H0L195.537 531H1254.54L1059 726ZM1326.74 459H267.735L463.272 264H1522.27L1326.74 459ZM1591.46 195H532.463L728 0H1787L1591.46 195Z" fill="black"/>
				</svg>
				<span class="text-xl font-bold tracking-tight">Stretch AI</span>
			</div>
		</div>
		<div class="hidden md:flex items-center gap-8 text-[13px] font-medium text-gray-600">
			<a href="#" class="hover:text-black transition-colors">Programs</a>
			<a href="#" class="hover:text-black transition-colors">Science</a>
			<a href="#" class="hover:text-black transition-colors">Pricing</a>
			<a href="#" class="hover:text-black transition-colors">FAQ</a>
			<a href="#" class="bg-black text-white px-5 py-2 rounded text-[13px] font-medium hover:bg-gray-800 transition-colors">Start free trial</a>
		</div>
	</nav>

	<!-- Hero Section -->
	<section class="flex flex-col items-center pt-16 pb-20 px-4 text-center">
		<h1 class="text-4xl md:text-[56px] leading-[1.1] font-medium tracking-tight max-w-3xl mb-6">
			Move better.<br>Perform longer.
		</h1>
		<p class="text-gray-500 text-[15px] max-w-xl mb-8 leading-relaxed">
			Expert-led mobility and stretching programs designed for athletes, trainers, and anyone serious about longevity. Science-backed protocols that actually work.
		</p>
		<button class="bg-black text-white px-6 py-3 rounded text-[13px] font-medium hover:bg-gray-800 transition-colors mb-20">
			Start your free trial
		</button>

		<!-- Horizontal Scroll Images -->
		<div class="w-full max-w-[1400px] overflow-hidden relative mt-12">
			<div class="flex gap-6 justify-center items-center h-[320px]">
				<!-- Image 1 -->
				<div class="w-[200px] h-[260px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[-2deg] translate-y-4">
					<img src="/generated/image-person-doing-a-deep-hip-flexor-stretch-o-1766105488969-0.webp" alt="Hip flexor stretch" class="w-full h-full object-cover" />
				</div>
				<!-- Image 2 -->
				<div class="w-[260px] h-[180px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[1deg] -translate-y-2">
					<img src="/generated/image-athlete-performing-a-shoulder-mobility-e-1766105491074-1.webp" alt="Shoulder mobility" class="w-full h-full object-cover" />
				</div>
				<!-- Image 3 -->
				<div class="w-[220px] h-[220px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[-1deg] translate-y-2">
					<img src="/generated/image-person-doing-a-hamstring-stretch-outdoor-1766105493131-2.webp" alt="Hamstring stretch" class="w-full h-full object-cover" />
				</div>
				<!-- Image 4 -->
				<div class="w-[200px] h-[200px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[2deg] -translate-y-4">
					<img src="/generated/image-runner-doing-a-quad-stretch-before-train-1766105495307-3.webp" alt="Quad stretch" class="w-full h-full object-cover" />
				</div>
				<!-- Image 5 -->
				<div class="w-[180px] h-[260px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[-2deg] translate-y-6">
					<img src="/generated/image-person-doing-a-spinal-twist-stretch-on-t-1766105497640-4.webp" alt="Spinal twist" class="w-full h-full object-cover" />
				</div>
				<!-- Image 6 -->
				<div class="w-[200px] h-[160px] rounded-[24px] overflow-hidden flex-shrink-0 relative group shadow-lg rotate-[1deg] -translate-y-2">
					<img src="/generated/image-athlete-performing-foam-rolling-for-reco-1766105499649-5.webp" alt="Foam rolling recovery" class="w-full h-full object-cover" />
				</div>
			</div>
		</div>
	</section>

	<!-- App Showcase -->
	<section class="py-24 px-6 md:px-12 flex justify-center">
		<div class="bg-white rounded-[32px] p-12 md:p-20 flex flex-col md:flex-row items-center gap-16 max-w-[1200px] w-full shadow-sm">
			<!-- Phone Mockup -->
			<div class="relative w-[280px] h-[580px] bg-black rounded-[40px] p-3 shadow-2xl flex-shrink-0 border-4 border-gray-100">
				<div class="w-full h-full bg-white rounded-[32px] overflow-hidden relative">
					<!-- Fake App UI -->
					<div class="p-6 pt-10">
						<div class="flex justify-between items-center mb-6">
							<div class="text-xs font-bold">Today's Session</div>
							<div class="w-6 h-6 bg-gray-200 rounded-full"></div>
						</div>
						<div class="bg-gradient-to-br from-primary-500 to-primary-700 p-4 rounded-xl mb-4 text-white">
							<div class="text-[10px] opacity-80 mb-1">MOBILITY PROTOCOL</div>
							<div class="text-lg font-bold mb-2">Hip Flexor Series</div>
							<div class="text-[10px] opacity-80">15 min • Intermediate</div>
						</div>
						<div class="space-y-3">
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 rounded-lg bg-green-100 flex items-center justify-center text-[10px] font-bold text-green-600">✓</div>
								<div class="flex-1">
									<div class="text-[10px] font-medium">Warm-up Flow</div>
									<div class="h-1 bg-green-100 rounded-full w-full mt-1"></div>
								</div>
							</div>
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 rounded-lg bg-primary-100 flex items-center justify-center text-[10px] font-bold text-primary-600">2</div>
								<div class="flex-1">
									<div class="text-[10px] font-medium">Hip Flexor Stretch</div>
									<div class="h-1 bg-gray-100 rounded-full w-full mt-1"></div>
								</div>
							</div>
							<div class="flex items-center gap-3">
								<div class="w-8 h-8 rounded-lg bg-gray-100 flex items-center justify-center text-[10px] font-bold text-gray-400">3</div>
								<div class="flex-1">
									<div class="text-[10px] font-medium text-gray-400">Cool Down</div>
									<div class="h-1 bg-gray-100 rounded-full w-full mt-1"></div>
								</div>
							</div>
						</div>
					</div>
					<!-- Bottom Nav -->
					<div class="absolute bottom-0 left-0 w-full h-16 bg-white border-t border-gray-100 flex justify-around items-center px-4">
						<div class="w-6 h-6 bg-black rounded-full"></div>
						<div class="w-6 h-6 bg-gray-200 rounded-full"></div>
						<div class="w-6 h-6 bg-gray-200 rounded-full"></div>
						<div class="w-6 h-6 bg-gray-200 rounded-full"></div>
					</div>
				</div>
			</div>

			<!-- Content -->
			<div class="flex-1 max-w-lg">
				<h2 class="text-3xl font-medium mb-6 leading-tight">
					Your mobility journey, simplified.<br>
					Follow expert-designed protocols, track your progress,
					and see measurable improvements in range of motion.
					Every session is structured, scientifically-backed,
					and built to help you move better for life.
				</h2>
				<div class="flex items-center justify-between mt-12">
					<a href="#" class="flex items-center gap-2 text-primary-600 text-sm font-medium hover:underline">
						{@html PlayCircle}
						Watch demo
					</a>
					<div class="flex gap-4">
						<button class="w-8 h-8 flex items-center justify-center rounded-full border border-gray-200 hover:bg-gray-50 transition-colors">
							{@html ChevronLeft}
						</button>
						<button class="w-8 h-8 flex items-center justify-center rounded-full border border-gray-200 hover:bg-gray-50 transition-colors">
							{@html ChevronRight}
						</button>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Lifestyle Grid -->
	<section class="py-20 px-6 md:px-12 max-w-[1400px] mx-auto w-full">
		<div class="flex flex-col md:flex-row justify-between items-start mb-16 gap-10">
			<h2 class="text-4xl md:text-5xl font-medium tracking-tight max-w-md leading-[1.1]">
				Built for those who take performance seriously.
			</h2>
			<p class="text-gray-500 text-[15px] max-w-md leading-relaxed">
				Whether you're an athlete, trainer, or fitness enthusiast, mobility is the foundation of longevity. Stretch AI gives you the structure, expertise, and consistency you need to move better, prevent injury, and perform at your peak.
			</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<!-- Card 1 -->
			<div class="relative h-[480px] rounded-[32px] overflow-hidden group">
				<img src="/generated/image-confident-female-athlete-in-her-30s-doin-1766105501646-6.webp" alt="Structured mobility routine" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
				<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent flex flex-col justify-end p-8 text-white">
					<h3 class="text-2xl font-medium mb-2">Expert-led protocols.</h3>
					<p class="text-sm text-white/80 leading-relaxed">No guesswork. Follow structured programs designed by sports scientists and physical therapists.</p>
				</div>
			</div>
			<!-- Card 2 -->
			<div class="relative h-[480px] rounded-[32px] overflow-hidden group">
				<img src="/generated/image-male-athlete-tracking-progress-on-his-ph-1766105503901-7.webp" alt="Tracking progress" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
				<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent flex flex-col justify-end p-8 text-white">
					<h3 class="text-2xl font-medium mb-2">Track real progress.</h3>
					<p class="text-sm text-white/80 leading-relaxed">Measure improvements in range of motion and see how consistency transforms your mobility.</p>
				</div>
			</div>
			<!-- Card 3 -->
			<div class="relative h-[480px] rounded-[32px] overflow-hidden group">
				<img src="/generated/image-person-doing-recovery-stretches-in-a-pea-1766105506054-8.webp" alt="Recovery and longevity" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
				<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent flex flex-col justify-end p-8 text-white">
					<h3 class="text-2xl font-medium mb-2">Prevent injury. Extend your career.</h3>
					<p class="text-sm text-white/80 leading-relaxed">Mobility work isn't optional—it's essential for longevity and peak performance.</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Testimonial -->
	<section class="py-24 px-6 text-center bg-[#F5F5F3]">
		<div class="max-w-3xl mx-auto">
			<blockquote class="text-2xl md:text-3xl font-medium leading-tight mb-10">
				"Stretch AI is what I've been recommending to my athletes for years—structured, evidence-based mobility work that actually delivers results. The protocols are clinically sound, and the platform makes it simple to stay consistent. This is the real deal."
			</blockquote>
			<div class="flex flex-col items-center gap-3">
				<img src="/generated/image-professional-physical-therapist-or-sport-1766105508492-9.webp" alt="Physical Therapist" class="w-12 h-12 rounded-full object-cover" />
				<div class="text-sm">
					<div class="font-bold">Dr. Marcus Chen, DPT</div>
					<div class="text-gray-500">Sports Physical Therapist</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Process Steps -->
	<section class="py-20 px-6 md:px-12 max-w-[1400px] mx-auto w-full border-b border-gray-200">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
			<div>
				<h3 class="text-xl font-medium mb-2">Sign up in 2 minutes.</h3>
				<p class="text-sm text-gray-500 leading-relaxed">Create your account, answer a few questions about your goals, and get instant access to all programs.</p>
			</div>
			<div>
				<h3 class="text-xl font-medium mb-2">Start your first session.</h3>
				<p class="text-sm text-gray-500 leading-relaxed">Follow expert-guided protocols designed for your level. Each session is clear, structured, and effective.</p>
			</div>
			<div>
				<h3 class="text-xl font-medium mb-2">Track your progress.</h3>
				<p class="text-sm text-gray-500 leading-relaxed">See measurable improvements in mobility and range of motion. Build consistency that lasts.</p>
			</div>
		</div>
	</section>

	<!-- How it works -->
	<section class="py-24 px-6 md:px-12 max-w-[1400px] mx-auto w-full">
		<div class="flex flex-col lg:flex-row gap-20">
			<!-- Sticky Title -->
			<div class="lg:w-1/3 lg:sticky lg:top-24 h-fit">
				<h2 class="text-4xl font-medium mb-6">How it works.</h2>
				<p class="text-gray-500 text-[15px] leading-relaxed max-w-xs">
					Stretch AI combines expert-designed protocols with intelligent tracking to deliver a complete mobility system. No guesswork, no generic routines—just proven methods that help you move better.
				</p>
			</div>

			<!-- Steps List -->
			<div class="lg:w-2/3 flex flex-col gap-8">
				<!-- Step 1 -->
				<div class="bg-white rounded-[32px] p-10 md:p-16 flex flex-col items-center text-center shadow-sm">
					<div class="w-full max-w-md mb-10 text-left self-start">
						<div class="w-8 h-8 rounded border border-gray-200 flex items-center justify-center text-xs font-medium mb-6">1</div>
						<h3 class="text-2xl font-medium mb-3">Choose your program.</h3>
						<p class="text-sm text-gray-500 leading-relaxed">Select from targeted programs for different goals—whether you're focused on recovery, performance, or injury prevention. All programs are designed by experts.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black rounded-[36px] p-2 shadow-xl border-4 border-gray-100">
						<div class="w-full h-full bg-white rounded-[28px] overflow-hidden relative flex flex-col">
                            <!-- Mock UI -->
                            <div class="bg-gray-50 p-4 border-b">
                                <div class="h-4 w-20 bg-gray-200 rounded mb-2"></div>
                            </div>
                            <div class="p-4 space-y-3">
                                <div class="h-12 bg-primary-50 rounded-lg border border-primary-100 p-2">
                                    <div class="h-2 w-16 bg-primary-200 rounded mb-1"></div>
                                    <div class="h-4 w-28 bg-primary-300 rounded"></div>
                                </div>
                                <div class="h-12 bg-white rounded-lg border border-gray-100 p-2">
                                    <div class="h-2 w-16 bg-gray-200 rounded mb-1"></div>
                                    <div class="h-4 w-28 bg-gray-300 rounded"></div>
                                </div>
                                <div class="h-12 bg-white rounded-lg border border-gray-100 p-2">
                                    <div class="h-2 w-16 bg-gray-200 rounded mb-1"></div>
                                    <div class="h-4 w-28 bg-gray-300 rounded"></div>
                                </div>
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 2 -->
				<div class="bg-white rounded-[32px] p-10 md:p-16 flex flex-col items-center text-center shadow-sm">
					<div class="w-full max-w-md mb-10 text-left self-start">
						<div class="w-8 h-8 rounded border border-gray-200 flex items-center justify-center text-xs font-medium mb-6">2</div>
						<h3 class="text-2xl font-medium mb-3">Follow guided sessions.</h3>
						<p class="text-sm text-gray-500 leading-relaxed">Each session provides clear video instruction and real-time guidance. Know exactly what to do, how long to hold, and when to progress.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black rounded-[36px] p-2 shadow-xl border-4 border-gray-100">
                        <div class="w-full h-full bg-white rounded-[28px] overflow-hidden relative flex flex-col items-center pt-8">
                            <div class="text-sm font-bold mb-4">Today's Session</div>
                            <div class="w-32 h-32 bg-gray-100 rounded-2xl mb-4 flex items-center justify-center">
                                <div class="w-0 h-0 border-l-[16px] border-l-black border-t-[12px] border-t-transparent border-b-[12px] border-b-transparent ml-1"></div>
                            </div>
                            <div class="text-xs text-gray-500 px-8 text-center">Hip Mobility Protocol</div>
                            <div class="text-xs text-gray-400 px-8 text-center mt-1">15 minutes</div>
                            <div class="mt-auto w-full p-4">
                                <div class="w-full h-10 bg-black rounded-lg"></div>
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 3 -->
				<div class="bg-white rounded-[32px] p-10 md:p-16 flex flex-col items-center text-center shadow-sm">
					<div class="w-full max-w-md mb-10 text-left self-start">
						<div class="w-8 h-8 rounded border border-gray-200 flex items-center justify-center text-xs font-medium mb-6">3</div>
						<h3 class="text-2xl font-medium mb-3">Track your improvements.</h3>
						<p class="text-sm text-gray-500 leading-relaxed">See measurable progress in range of motion and mobility scores. The platform tracks your consistency and shows how you're improving over time.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black rounded-[36px] p-2 shadow-xl border-4 border-gray-100">
                        <div class="w-full h-full bg-gray-900 rounded-[28px] overflow-hidden relative text-white p-6 pt-10">
                             <div class="flex items-center gap-3 mb-6">
                                 <div class="w-10 h-10 rounded-full bg-gray-700"></div>
                                 <div>
                                     <div class="text-sm font-bold">Your Progress</div>
                                     <div class="text-[10px] text-gray-400">Week 4</div>
                                 </div>
                             </div>
                             <div class="space-y-2">
                                 <div class="h-20 bg-gray-800 rounded-xl p-3">
                                     <div class="text-[10px] text-gray-400 mb-1">Hip Mobility</div>
                                     <div class="flex items-center gap-2">
                                         <div class="flex-1 h-2 bg-gray-700 rounded-full overflow-hidden">
                                             <div class="h-full bg-primary-500 w-3/4"></div>
                                         </div>
                                         <div class="text-xs">+12%</div>
                                     </div>
                                 </div>
                                 <div class="h-20 bg-gray-800 rounded-xl p-3">
                                     <div class="text-[10px] text-gray-400 mb-1">Shoulder ROM</div>
                                     <div class="flex items-center gap-2">
                                         <div class="flex-1 h-2 bg-gray-700 rounded-full overflow-hidden">
                                             <div class="h-full bg-primary-500 w-2/3"></div>
                                         </div>
                                         <div class="text-xs">+8%</div>
                                     </div>
                                 </div>
                             </div>
                        </div>
					</div>
				</div>

				<!-- Step 4 -->
				<div class="bg-white rounded-[32px] p-10 md:p-16 flex flex-col items-center text-center shadow-sm">
					<div class="w-full max-w-md mb-10 text-left self-start">
						<div class="w-8 h-8 rounded border border-gray-200 flex items-center justify-center text-xs font-medium mb-6">4</div>
						<h3 class="text-2xl font-medium mb-3">Get personalized insights.</h3>
						<p class="text-sm text-gray-500 leading-relaxed">Receive expert guidance on areas to focus on, modifications for your body, and recommendations to accelerate your progress.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black rounded-[36px] p-2 shadow-xl border-4 border-gray-100">
                        <div class="w-full h-full bg-white rounded-[28px] overflow-hidden relative flex flex-col pt-8 px-4">
                            <div class="text-center text-sm font-bold mb-4">Insights</div>
                            <div class="text-[10px] text-gray-500 leading-relaxed text-justify">
                                Your hip mobility has improved significantly over the past 3 weeks. Consider adding the Advanced Hip Protocol to continue this momentum.
                                <br><br>
                                Your shoulder range of motion shows asymmetry. Focus on the Shoulder Stability series to address this imbalance...
                            </div>
                        </div>
					</div>
				</div>

				<!-- Step 5 -->
				<div class="bg-white rounded-[32px] p-10 md:p-16 flex flex-col items-center text-center shadow-sm">
					<div class="w-full max-w-md mb-10 text-left self-start">
						<div class="w-8 h-8 rounded border border-gray-200 flex items-center justify-center text-xs font-medium mb-6">5</div>
						<h3 class="text-2xl font-medium mb-3">Build lasting habits.</h3>
						<p class="text-sm text-gray-500 leading-relaxed">Consistency is key. The platform helps you build a sustainable mobility practice that becomes part of your routine, not another thing to stress about.</p>
					</div>
					<div class="w-[240px] h-[480px] bg-black rounded-[36px] p-2 shadow-xl border-4 border-gray-100">
                        <div class="w-full h-full bg-white rounded-[28px] overflow-hidden relative flex flex-col pt-8 px-4">
                             <div class="bg-gray-100 p-3 rounded-lg text-[10px] mb-2">
                                 Why is consistency more important than intensity?
                             </div>
                             <div class="text-[10px] text-gray-500 leading-relaxed mt-2">
                                 Mobility improvements come from regular, progressive work—not occasional intense sessions. Your nervous system adapts through repetition and consistency...
                             </div>
                        </div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Dark Cards Section -->
	<section class="py-10 px-6 md:px-12 max-w-[1400px] mx-auto w-full">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			<!-- Left Card -->
			<div class="bg-[#111] rounded-[32px] p-10 md:p-12 text-white min-h-[400px] flex flex-col relative overflow-hidden">
				<div class="relative z-10">
					<div class="text-xs text-gray-400 mb-2">Evidence-based approach.</div>
					<h3 class="text-2xl font-medium max-w-xs">Designed by sports scientists and physical therapists.</h3>
				</div>
				<!-- Abstract mobility graphic -->
				<div class="absolute bottom-0 right-0 w-full h-64 opacity-20">
                    <svg viewBox="0 0 200 100" class="w-full h-full">
                        <path d="M20,80 Q50,20 80,50 T140,40" stroke="white" stroke-width="2" fill="none" />
                        <path d="M30,70 Q60,30 90,60 T150,50" stroke="white" stroke-width="2" fill="none" />
                        <circle cx="80" cy="50" r="3" fill="white" />
                        <circle cx="140" cy="40" r="3" fill="white" />
                    </svg>
				</div>
			</div>
			<!-- Right Card -->
			<div class="bg-[#111] rounded-[32px] p-10 md:p-12 text-white min-h-[400px] flex flex-col relative overflow-hidden">
				<div class="relative z-10">
					<div class="text-xs text-gray-400 mb-2">Your data is secure.</div>
					<h3 class="text-2xl font-medium max-w-xs">Privacy-first platform built for professionals.</h3>
				</div>
				<!-- Encrypted data visual -->
				<div class="absolute bottom-8 right-8 text-right font-mono text-3xl opacity-30 blur-[2px] select-none pointer-events-none">
					<div>Progr|%s$9yT</div>
					<div>Mobil|I7y/@</div>
					<div>Range|&5a!</div>
					<div>Flexib|?Pm_Lw</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Pricing Section -->
	<section class="py-24 px-6 md:px-12 max-w-[1400px] mx-auto w-full text-center">
		<h2 class="text-3xl md:text-4xl font-medium mb-4">Invest in your mobility.</h2>
		<p class="text-gray-500 text-sm max-w-lg mx-auto mb-16">
			Expert-designed programs, intelligent tracking, and personalized guidance—all in one platform. Choose the plan that fits your goals.
		</p>

		<div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-4xl mx-auto">
			<!-- Monthly Plan -->
			<div class="bg-white rounded-[32px] p-8 text-left flex flex-col shadow-sm">
				<div class="w-10 h-10 bg-gray-100 rounded-lg mb-6"></div>
				<h3 class="text-xl font-bold mb-1">Monthly</h3>
				<p class="text-xs text-gray-500 mb-6">Try it out, cancel anytime.</p>
				
				<div class="flex items-baseline gap-1 mb-1">
					<span class="text-2xl font-bold">$29</span>
					<span class="text-xs text-gray-500">/month</span>
				</div>
				<div class="text-[10px] text-gray-400 mb-8">First month free with code MOVE30</div>

				<ul class="space-y-4 mb-8 flex-1">
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Access to all mobility and stretching programs
					</li>
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Progress tracking and mobility assessments
					</li>
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Expert video instruction for every movement
					</li>
				</ul>

				<button class="w-full bg-black text-white py-3 rounded-lg text-xs font-bold hover:bg-gray-800 transition-colors">Start free trial</button>
			</div>

			<!-- Annual Plan -->
			<div class="bg-white rounded-[32px] p-8 text-left flex flex-col shadow-sm border-2 border-primary-100 relative overflow-hidden">
                <div class="absolute top-0 right-0 bg-primary-100 text-primary-700 text-[10px] font-bold px-3 py-1 rounded-bl-xl">BEST VALUE</div>
				<div class="w-10 h-10 bg-primary-50 rounded-lg mb-6"></div>
				<h3 class="text-xl font-bold mb-1">Annual</h3>
				<p class="text-xs text-gray-500 mb-6">Save 40% with annual billing.</p>
				
				<div class="flex items-baseline gap-1 mb-1">
					<span class="text-2xl font-bold">$199</span>
					<span class="text-xs text-gray-500">/year</span>
				</div>
				<div class="text-[10px] text-gray-400 mb-8">Just $16.58/month — save $149 annually</div>

				<ul class="space-y-4 mb-8 flex-1">
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Everything in Monthly, plus priority support
					</li>
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Early access to new programs and features
					</li>
					<li class="flex gap-3 text-xs text-gray-600">
						<span class="text-green-500 shrink-0">{@html Check}</span>
						Personalized program recommendations and insights
					</li>
				</ul>

				<button class="w-full bg-black text-white py-3 rounded-lg text-xs font-bold hover:bg-gray-800 transition-colors">Start free trial</button>
			</div>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-20 px-6 md:px-12 max-w-3xl mx-auto w-full">
		<h2 class="text-3xl font-medium text-center mb-16">Your questions answered.</h2>
		<div class="space-y-4">
			{#each faqs as faq, i}
				<button 
					class="w-full flex items-center justify-between p-4 text-left hover:bg-gray-100 rounded-lg transition-colors group"
					onclick={() => toggleFaq(i)}
				>
					<span class="text-sm font-medium text-gray-800">{faq.question}</span>
					<span class="text-gray-400 transition-transform duration-200 {faq.open ? 'rotate-45' : ''}">{@html Plus}</span>
				</button>
                {#if faq.open}
                    <div class="px-4 pb-4 text-xs text-gray-500 leading-relaxed">
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
			<button class="bg-white border border-gray-200 px-6 py-3 rounded text-xs font-medium hover:bg-gray-50 transition-colors">
				View all Frequently Asked Questions
			</button>
		</div>
	</section>

	<!-- Footer -->
	<footer class="bg-[#F5F5F3] py-16 px-6 md:px-12 text-[11px] text-gray-500">
		<div class="max-w-[1400px] mx-auto">
			<div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-12 gap-8">
				<div class="flex items-center gap-3">
					<svg width="40" height="16" viewBox="0 0 1787 726" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M1059 726H0L195.537 531H1254.54L1059 726ZM1326.74 459H267.735L463.272 264H1522.27L1326.74 459ZM1591.46 195H532.463L728 0H1787L1591.46 195Z" fill="black"/>
					</svg>
					<span class="text-lg font-bold tracking-tight text-black">Stretch AI</span>
				</div>
				<div class="flex flex-wrap gap-6 font-medium text-gray-600">
					<a href="#" class="hover:text-black">Programs</a>
					<a href="#" class="hover:text-black">Science</a>
					<a href="#" class="hover:text-black">Pricing</a>
					<a href="#" class="hover:text-black">FAQ</a>
					<a href="#" class="hover:text-black">Terms & Conditions</a>
					<a href="#" class="hover:text-black">Privacy Policy</a>
				</div>
				<div class="flex gap-4">
					<a href="#" class="text-black hover:text-gray-600">{@html XIcon}</a>
					<a href="#" class="text-black hover:text-gray-600">{@html Instagram}</a>
					<a href="#" class="text-black hover:text-gray-600">{@html Linkedin}</a>
				</div>
			</div>
			
			<div class="space-y-4 leading-relaxed opacity-60">
				<p>Stretch AI is a digital platform providing mobility and stretching guidance. Our programs are designed by qualified professionals but do not constitute medical advice, diagnosis, or treatment. Always consult with a healthcare provider before starting any new exercise program, especially if you have existing injuries or medical conditions.</p>
				<p>Results may vary based on individual commitment, consistency, and physical condition. The testimonials and progress examples shown represent individual experiences and are not guarantees of specific results.</p>
				<p>By subscribing, you agree to our Terms & Conditions and Privacy Policy. You can cancel your subscription at any time. Message and data rates may apply for SMS notifications.</p>
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

