## videoView using mediaControler

#### Riview
![1](https://user-images.githubusercontent.com/43386555/54184704-d98d0300-44d9-11e9-87a5-de745065bf5d.gif)

### sourece
____________
        VideoView videoView = (VideoView) findViewById(R.id.videoView);

        videoView.setVideoPath("android.resource://" + getPackageName() + "/" + R.raw.a);

        MediaController mediaController = new MediaController(this);

        //setting mediaControler in videoView
        mediaController.setAnchorView(videoView);

        //setting videoView using mediaControler
        videoView.setMediaController(mediaController);

        videoView.start();
    }
