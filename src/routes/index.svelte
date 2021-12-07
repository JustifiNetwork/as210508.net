<section>
  <h1>
    <img src="/wordmark.svg" alt="as210508" />
  </h1>
</section>

<section>
  <h2>About</h2>

  <p>
    AS210508 is a production IPv4 and IPv6 network run by Justifi Network to provide networking and
    hosting solutions to our clients
  </p>

  <div class="link-list">
    <a target="_blank" href="#abuse">Abuse</a>
    <a target="_blank" href="https://www.peeringdb.com/asn/210508">PeeringDB</a>
    <a target="_blank" href="https://bgp.tools/as/210508">BGP Tools</a>
    <a target="_blank" href="https://bgp.he.net/AS210508">BGP.HE.NET</a>
    <a target="_blank" href="https://radar.qrator.net/as210508">QRATOR</a>
    <a target="_blank" href="https://irrexplorer.nlnog.net/asn/AS210508">IRR Explorer</a>
    <a target="_blank" href="https://ipinfo.io/AS210508">IPinfo</a>
  </div>
</section>

<section>
  <h2>Points of Presence</h2>

  <h3>nyc01 - New Jersey</h3>
  <div class="prefixes">
    <small>IPv6</small>
    <p>2602:fc26:a0::/45</p>
    <small>IPv4</small>
    <p>192.168.168.0/24</p>
  </div>

  <h3>sthlm01 - Stockholm</h3>
  <div class="prefixes">
    <small>IPv6</small>
    <p>2602:fc26:a8::/45</p>
  </div>
</section>

<style lang="scss">
  section {
    * + * {
      margin-top: 1em;
    }

    & + section {
      margin-top: 5rem;
    }

    h2 {
      font-size: 2rem;
      padding-bottom: 0.25rem;
      border-bottom: 1px #ddd solid;
      position: relative;

      &:hover::after {
        width: 5rem;
      }

      &::after {
        content: '';
        position: absolute;
        left: 0;
        bottom: -0.125rem;
        height: 0.25rem;
        width: 2.5rem;
        background: var(--cold-winds);
        transition: width 300ms ease;
      }
    }

    h3 {
      font-size: 2rem;
    }

    .link-list {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      gap: 1rem;

      a {
        margin: 0;
        color: var(--almost-black);
        text-decoration: none;
        border-bottom: 1px solid #ddd;
        padding-bottom: 0.125rem;
        position: relative;

        &:hover::after {
          width: 100%;
        }

        &::after {
          content: '';
          position: absolute;
          left: 0;
          bottom: -0.125rem;
          height: 0.125rem;
          width: 1rem;
          background: var(--cold-winds);
          transition: width 300ms ease;
        }
      }
    }
  }

  h1 {
    img {
      width: 100%;
    }
  }

  .prefixes {
    small {
      font-size: 0.75rem;
      font-weight: bold;
    }
    small + p {
      margin-top: 0;
    }
  }
</style>
