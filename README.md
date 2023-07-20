# HLS-video-player-
<code>
String player_applicationId = "com.online.player";
try {
    Intent sendIntent = new Intent(Intent.ACTION_SEARCH);
    sendIntent.setPackage(player_applicationId);
    sendIntent.putExtra("video_title", "Sample_videos");
    sendIntent.putExtra("video_url", "https://download.nemosofts.com/sample_videos.mp4");
    sendIntent.putExtra("video_agent", "");
    // videoType = normal or youtube or webview
    sendIntent.putExtra("video_type", "normal");
    sendIntent.setType("text/plain");
    sendIntent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
    startActivity(sendIntent);
} catch (Exception e) {
    e.printStackTrace();
    startActivity(new Intent(Intent.ACTION_VIEW, Uri.parse("http://play.google.com/store/apps/details?id=" + player_applicationId)));
}
</code>
