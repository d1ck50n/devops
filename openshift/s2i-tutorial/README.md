To create a sample app using s2i image:
1. Go into s2i-tutorial/custom_s2i and running `podman build -t my-s2i .`
2. Go to s2i-tutorial and running `s2i build test-app-src/  my-s2i sample-app --as-dockerfile sample-app/Dockerfile`
3. Go to s2i-tutorial/sample-app, and running `podman build -t my-s2i-app .`
4. Run `podman run -p 8080:8080 -d my-s2i-app`
5. Test by running `curl http://localhost:8080`
