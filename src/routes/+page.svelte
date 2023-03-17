<script lang="ts">
    import AddManifest from "$lib/components/AddManifest.svelte";
    import { MetaTags } from 'svelte-meta-tags'
</script>

<div class="p-8 md:p-20">
    <h1 class="font-bold text-[20px]">What would you like to <span class="text-[#8D86C9]">manifest</span> into your life right <span class="text-[#8D86C9]">now</span>?</h1>
    <AddManifest />
</div>

<MetaTags
  title="Manifest.me"
  titleTemplate="%s | Svelte Meta Tags"
  description="A simple app to help you manifest your desires"
  openGraph={{
    url: 'https://manifest-me.vercel.app/',
    title: 'Manifest.me',
    description: 'A simple app to help you manifest your desires',
    images: [
      {
        url: 'https://imgur.com/vXFHcc5',
        width: 1920,
        height: 1080,
        alt: 'manifest.me preview image'
      },
    ],
  }}
  twitter={{
    handle: '@handle',
    site: '@site',
    cardType: 'summary_large_image',
    title: 'Manifest.me',
    description: 'A simple app to help you manifest your desires',
    image: 'https://imgur.com/vXFHcc5',
    imageAlt: 'Twitter image alt'
  }}

/>