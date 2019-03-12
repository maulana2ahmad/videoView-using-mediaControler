## videoView using mediaControler

### sourece
____________
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        VideoView videoView = (VideoView) findViewById(R.id.videoView);

        videoView.setVideoPath("android.resource://" + getPackageName() + "/" + R.raw.a);

        MediaController mediaController = new MediaController(this);

        //setting mediaControler in videoView
        mediaController.setAnchorView(videoView);

        //setting videoView using mediaControler
        videoView.setMediaController(mediaController);

        videoView.start();
    }
