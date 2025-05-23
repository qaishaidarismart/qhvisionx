<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calamansi Pistachio Cod Reel</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <style>
        body {
            background-color: #000;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }
        
        .instagram-container {
            max-width: 414px;
            margin: 0 auto;
            position: relative;
            height: 100vh;
            background-color: #000;
            overflow: hidden;
        }
        
        .video-container {
            position: relative;
            width: 100%;
            height: 100%;
            overflow: hidden;
            background-color: #000;
        }
        
        .video-clip {
            position: absolute;
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: none;
        }
        
        .active-clip {
            display: block;
        }
        
        .caption {
            position: absolute;
            bottom: 120px;
            left: 15px;
            right: 15px;
            color: white;
            padding: 10px 15px;
            border-radius: 8px;
            background-color: rgba(0, 0, 0, 0.5);
            font-size: 16px;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
        }
        
        .instagram-ui {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 20;
        }
        
        .top-bar {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 15px;
            background: linear-gradient(to bottom, rgba(0,0,0,0.6) 0%, rgba(0,0,0,0) 100%);
        }
        
        .bottom-bar {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 15px;
            background: linear-gradient(to top, rgba(0,0,0,0.6) 0%, rgba(0,0,0,0) 100%);
        }
        
        .progress-container {
            display: flex;
            justify-content: space-between;
            position: absolute;
            top: 65px;
            left: 15px;
            right: 15px;
            height: 3px;
            z-index: 30;
        }
        
        .progress-segment {
            flex: 1;
            height: 100%;
            background-color: rgba(255, 255, 255, 0.3);
            margin: 0 2px;
            border-radius: 3px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            width: 0%;
            background-color: white;
        }
        
        .side-actions {
            position: absolute;
            right: 15px;
            bottom: 150px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .side-action {
            margin: 12px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .side-action i {
            font-size: 28px;
            color: white;
            margin-bottom: 4px;
        }
        
        .side-action span {
            font-size: 12px;
            color: white;
        }
        
        .user-info {
            display: flex;
            align-items: center;
        }
        
        .user-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: #f56040;
            margin-right: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .comment-box {
            display: flex;
            align-items: center;
            margin-top: 15px;
        }
        
        .comment-input {
            flex: 1;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            color: white;
            padding: 8px 15px;
            font-size: 14px;
        }

        .loader {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s linear infinite;
            z-index: 40;
        }

        @keyframes spin {
            to {
                transform: translate(-50%, -50%) rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="instagram-container">
        <div class="video-container" id="video-container">
            <div class="loader" id="loader"></div>
            
            <!-- Video clips -->
            <video class="video-clip" id="clip-1" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/a824d507-5c08-4ed5-97aa-469b2d695474" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-2" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/14ea8cf1-500f-4d95-8a64-a896d3e67e18" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-3" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/7b79a669-8ea2-4e45-b66a-0469cb6e6370" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-4" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/f947a6af-c9dd-444e-8f4d-369ae4083704" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-5" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/ee52bc79-85e3-42fa-8007-b956eecfbd0f" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-6" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/bae90ccb-116d-47d9-853c-058915f069a2" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-7" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/39c64b81-c6c9-4b19-bf89-09d577bb361d" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-8" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/6ba3357d-e053-4eb8-b50c-382993db75a6" type="video/mp4">
            </video>
            
            <video class="video-clip" id="clip-9" playsinline muted>
                <source src="https://cdn1.genspark.ai/user-upload-image/5/4ed8d2fb-9bae-41c4-993e-a9bd4f467877" type="video/mp4">
            </video>
            
            <!-- Audio clips -->
            <audio id="audio-1" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/5166f89b-0664-400b-8c56-b1e59615d612" type="audio/mp3">
            </audio>
            
            <audio id="audio-2" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/9b7e8f3c-147f-4968-9076-9c55fdc6e272" type="audio/mp3">
            </audio>
            
            <audio id="audio-3" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/a0e22788-c103-432f-8ead-a559ca4ce4a3" type="audio/mp3">
            </audio>
            
            <audio id="audio-4" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/5cfc0ee5-bd62-4c80-a494-de3dbfa2fc45" type="audio/mp3">
            </audio>
            
            <audio id="audio-5" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/f9d1b6c8-8208-4524-82ac-5b9fb4eb1129" type="audio/mp3">
            </audio>
            
            <audio id="audio-6" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/30f8bf6e-ffba-49a6-906a-a134edad60e3" type="audio/mp3">
            </audio>
            
            <audio id="audio-7" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/172bd60e-54d5-4a70-820e-3421486f6232" type="audio/mp3">
            </audio>
            
            <audio id="audio-8" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/fefef71e-93d5-446c-9331-c92551e3d074" type="audio/mp3">
            </audio>
            
            <audio id="audio-9" preload="auto">
                <source src="https://cdn1.genspark.ai/user-upload-image/2/8ceac087-5ef7-456c-a5da-c80482d26104" type="audio/mp3">
            </audio>
            
            <div class="caption" id="caption"></div>
        </div>
        
        <div class="instagram-ui">
            <div class="top-bar">
                <div class="user-info">
                    <div class="user-avatar">C</div>
                    <span style="color: white; font-weight: bold;">Chef_Influencer</span>
                </div>
                <i class="fas fa-ellipsis-h" style="color: white;"></i>
            </div>
            
            <div class="progress-container" id="progress-container">
                <!-- Progress segments will be added here via JavaScript -->
            </div>
            
            <div class="side-actions">
                <div class="side-action">
                    <i class="fas fa-heart"></i>
                    <span>124k</span>
                </div>
                <div class="side-action">
                    <i class="fas fa-comment"></i>
                    <span>1,892</span>
                </div>
                <div class="side-action">
                    <i class="fas fa-paper-plane"></i>
                    <span>Share</span>
                </div>
                <div class="side-action">
                    <i class="fas fa-bookmark"></i>
                    <span>Save</span>
                </div>
            </div>
            
            <div class="bottom-bar">
                <div style="color: white; font-weight: bold;">🐟✨ CALAMANSI & PISTACHIO CRUSTED COD ✨🐟</div>
                <div style="color: #ccc; font-size: 14px; margin-top: 5px;">Elevating simple cod with bright Filipino calamansi citrus and crunchy pistachios!</div>
                <div class="comment-box">
                    <div class="comment-input">Add a comment...</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const captions = [
                "Start by zesting fresh calamansi - these small citrus fruits add a unique tangy flavor!",
                "Marinate the cod fillets in fresh calamansi juice, soy sauce, garlic, and honey",
                "Pulse the pistachios until coarsely ground - keep some texture for the perfect crust!",
                "Combine ground pistachios with panko, calamansi zest, parsley, garlic, and spices",
                "Sear the cod fillets presentation-side down until golden",
                "Flip the fish and generously press on the pistachio crust",
                "Transfer to a 400°F oven and bake for 8-10 minutes",
                "Check if it's done by gently flaking with a fork - it should be opaque and flaky",
                "Plate and garnish with fresh calamansi and extra pistachios - Calamansi and Pistachio Crusted Cod ready to enjoy!"
            ];
            
            const totalClips = 9;
            let currentClip = 0;
            let progressSegments = [];
            let progressFills = [];
            
            // Create progress segments
            const progressContainer = document.getElementById('progress-container');
            for (let i = 0; i < totalClips; i++) {
                const segment = document.createElement('div');
                segment.className = 'progress-segment';
                
                const fill = document.createElement('div');
                fill.className = 'progress-fill';
                segment.appendChild(fill);
                
                progressContainer.appendChild(segment);
                progressSegments.push(segment);
                progressFills.push(fill);
            }
            
            const captionElement = document.getElementById('caption');
            const loader = document.getElementById('loader');
            let videoElements = [];
            let audioElements = [];
            
            for (let i = 1; i <= totalClips; i++) {
                videoElements.push(document.getElementById(`clip-${i}`));
                audioElements.push(document.getElementById(`audio-${i}`));
            }
            
            function preloadVideos() {
                let loadedCount = 0;
                const totalMedia = videoElements.length + audioElements.length;
                
                function checkAllLoaded() {
                    loadedCount++;
                    if (loadedCount >= totalMedia) {
                        loader.style.display = 'none';
                        startPlayback();
                    }
                }
                
                videoElements.forEach(video => {
                    video.addEventListener('canplaythrough', checkAllLoaded, { once: true });
                    video.load();
                });
                
                audioElements.forEach(audio => {
                    audio.addEventListener('canplaythrough', checkAllLoaded, { once: true });
                    audio.load();
                });
                
                // Fallback in case events don't fire
                setTimeout(() => {
                    if (loadedCount < totalMedia) {
                        loader.style.display = 'none';
                        startPlayback();
                    }
                }, 5000);
            }
            
            function startPlayback() {
                playClip(0);
            }
            
            function updateProgressBar(clipIndex, progress) {
                progressFills[clipIndex].style.width = `${progress * 100}%`;
            }
            
            function playClip(index) {
                if (index >= totalClips) {
                    // Restart the reel when finished
                    setTimeout(() => {
                        resetProgressBars();
                        playClip(0);
                    }, 2000);
                    return;
                }
                
                // Reset all videos
                videoElements.forEach((video, i) => {
                    if (i !== index) {
                        video.pause();
                        video.currentTime = 0;
                        video.classList.remove('active-clip');
                    }
                });
                
                // Stop all audio
                audioElements.forEach((audio, i) => {
                    if (i !== index) {
                        audio.pause();
                        audio.currentTime = 0;
                    }
                });
                
                // Set current caption
                captionElement.textContent = captions[index];
                captionElement.style.opacity = 1;
                
                currentClip = index;
                
                const video = videoElements[index];
                const audio = audioElements[index];
                
                video.classList.add('active-clip');
                
                // Play video and audio together
                const playPromise = video.play();
                
                if (playPromise !== undefined) {
                    playPromise.then(_ => {
                        audio.play();
                        
                        // Set up progress tracking
                        const updateInterval = setInterval(() => {
                            if (!video.paused && video.duration > 0) {
                                const progress = video.currentTime / video.duration;
                                updateProgressBar(index, progress);
                            }
                        }, 50);
                        
                        // When clip ends, play next one
                        video.onended = () => {
                            clearInterval(updateInterval);
                            updateProgressBar(index, 1);
                            
                            // Hide caption with fade out
                            captionElement.style.opacity = 0;
                            
                            // Short delay before next clip
                            setTimeout(() => {
                                playClip(index + 1);
                            }, 300);
                        };
                    }).catch(error => {
                        console.error("Playback failed:", error);
                        // Try to continue to next clip on error
                        setTimeout(() => {
                            playClip(index + 1);
                        }, 1000);
                    });
                }
            }
            
            function resetProgressBars() {
                progressFills.forEach(fill => {
                    fill.style.width = '0%';
                });
            }
            
            // Click/tap to navigate between clips
            document.getElementById('video-container').addEventListener('click', function(e) {
                const containerWidth = this.offsetWidth;
                const clickX = e.offsetX;
                
                if (clickX < containerWidth / 3) {
                    // Left third - go back
                    if (currentClip > 0) {
                        playClip(currentClip - 1);
                    }
                } else if (clickX > containerWidth * 2 / 3) {
                    // Right third - go forward
                    if (currentClip < totalClips - 1) {
                        playClip(currentClip + 1);
                    }
                }
            });
            
            // Start loading videos
            preloadVideos();
        });
    </script>
</body>
</html>
