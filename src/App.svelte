<script>
  import "./styles.scss";
  import Form from "./components/Form.svelte";
  export let name;
</script>

<nav class="navbar">
  <div class="navbar-brand">
    <div class="navbar-item">
      <Form />
    </div>

    <div class="navbar-item">
      <div class="loader is-hidden" id="spinner" />
    </div>
  </div>
</nav>

<div class="container">
  <div class="columns ">
    <div
      class="profile-container column is-half-tablet is-one-third-widescreen">
      <h2 class="subtitle is-4">Profile</h2>

      <div class="profile">
        <div class="media">
          <div class="media-left">
            <figure class="media-left image is-64x64">
              <img src="http://placekitten.com/200/200" id="profile-image" />
            </figure>
          </div>
          <div class="media-content">
            <p class="title is-5" id="profile-name">John Smith</p>
            <p class="subtitle is-6">
              <a href="#" id="profile-url">@johnsmith</a>
            </p>
          </div>
        </div>

        <div class="content" id="profile-bio">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin
            ornare magna eros, eu pellentesque tortor vestibulum ut.
          </p>
        </div>
      </div>
    </div>

    <div class="events-container column">
      <h2 class="subtitle is-4">History</h2>

      <div class="timeline" id="user-timeline">
        <div class="timeline-item">
          <div class="timeline-marker" />
          <div class="timeline-content">
            <p class="heading">Jan 21, 2016</p>
            <div class="content">
              <!-- "user image ... is not aligned properly". I don't know how you wanted it to be alligned so i assumed that it only lack margin and text to be more 'around'. 
          Otherwise we need to pull <> username out of span and make other containers to play with position, but then gh-username will be invalid name, more like gh-useravatar. 
        -->
              <span class="gh-username is-flex">
                <img src="https://avatars.githubusercontent.com/u/2310778?" />
                <a href="https://github.com/sethii">sethii</a>
              </span>
              closed
              <a href="https://github.com/TheSoftwareHouse/Kakunin/pull/41">
                pull request
              </a>
              <p class="repo-name">
                <a href="https://github.com/TheSoftwareHouse/Kakunin">
                  TheSoftwareHouse/Kakunin
                </a>
              </p>
            </div>
          </div>
        </div>

        <div class="timeline-item is-primary">
          <div class="timeline-marker is-primary" />
          <div class="timeline-content">
            <p class="heading">Jan 19, 2016</p>
            <div class="content">
              <span class="gh-username is-flex">
                <img src="https://avatars.githubusercontent.com/u/1208786?" />
                <a href="https://github.com/simonsipl">gajdus</a>
              </span>
              created
              <a
                href="https://github.com/TheSoftwareHouse/Kakunin/pull/41#discussion_r176273897">
                comment
              </a>
              to
              <a
                href="https://api.github.com/repos/TheSoftwareHouse/Kakunin/pulls/comments/176273897">
                pull request
              </a>
              <p class="repo-name">
                <a href="https://github.com/TheSoftwareHouse/Kakunin">
                  TheSoftwareHouse/Kakunin
                </a>
              </p>
            </div>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-marker" />
          <div class="timeline-content">
            <p class="heading">Jan 19, 2016</p>
            <div class="content">
              <span class="gh-username is-flex">
                <img src="https://avatars.githubusercontent.com/u/2310778" />
                <a href="https://github.com/aherok">sethii</a>
              </span>
              opened
              <a href="https://github.com/TheSoftwareHouse/Kakunin/pull/41">
                pull request
              </a>
              <p class="repo-name">
                <a href="https://github.com/TheSoftwareHouse/Kakunin">
                  TheSoftwareHouse/Kakunin
                </a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
