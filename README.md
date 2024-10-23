  This is a "SIMPLE IMAGE GALLERY APP"

  SUMMARY : This is an iOS application that allows users to search and browse photos from Unsplash using the Unsplash API. The app features a smooth and responsive UI,
            supporting both dark and light modes, with infinite scrolling to load more images as the user scrolls.It uses the MVVM architecture to keep the code modular
            and maintainable.I have added activity Indicator also while loading data and after searching images by user.So that it will be helpful for them to give them 
            assurity that something is loading.And I have implemented serach bar aslo so that user can easily search for their favorite images as per their need.
           

a.How to run the project.

1.Clone the repository: https://github.com/deepalisabale/Image-Gallery-App.git
2.Navigate to the project folder: cd Image-Gallery-App
3.Install the project dependencies: pod install
4.Open the .xcworkspace file in Xcode: open Image Gallery App.xcworkspace
5.Select a simulator or connect a real device and run the project by pressing Cmd + R or by clicking the play button in Xcode.


b.Any challenges you faced and how you solved them.

1.Initially i didin't understand how to get API from unsplash .But after searching over internet i got some ideas. I have log in first and then got one access key and base URL for thta
I have gone through the documentation part also.I got one URL ( curl -H "Authorization: Client-ID YOUR_ACCESS_KEY" "https://api.unsplash.com/photos") .
I have run the above command by replacing my unique access key and client id .After running this command in terminal i got API Response.Accordingly i have created and my model class
and build my project.

2. Pagination and Infinite Scrolling was a little bit difficult to implement scroll view to load  more images when users scrolls down .For that i have conform to UIScrollViewDelegate method in extension and  Added logic in the scrollViewDidScroll method to detect when the user is near the bottom of the list and trigger the loadMorePhotos() function in the ViewModel.
   
3 Adapting the app's appearance for both dark and light modes, especially with placeholders and background colors.For implementing this functinality
  I have Used UIColor { traitCollection in ... } to dynamically switch colors based on the user interface style. This ensured a consistent experience across different modes 
              without needing to duplicate UI code.

c.Why you chose specific libraries (if any).

1.Kingfisher:
   Kingfisher simplifies asynchronous image downloading and caching, allowing us to avoid manual memory management and increase app performance. 
   Its built-in caching helps reduce redundant network calls and improves user experience with fast image loading.
2.Cocoapods:
 To manage external dependencies like Kingfisher easily and ensure a smooth installation process for any future dependencies.
 So that one can install any third party library as per their future need by editing the pod file.



 d.Brief explanation of your architecture choices.
 
 MVVM Architecture  :The MVVM (Model-View-ViewModel) architecture separates the business logic (ViewModel) from the UI (ViewController), making the code more modular and testable.
                     By binding the ViewModel to the ViewController, the UI updates automatically whenever the data changes, reducing the risk of tight coupling between the layers.
                     MVVM Architecture is folder structure so that one can simply get the idea after looking into the project which files are there under which folder.It will be helpful
                     to understand the project module.

  //Loom Video Link : https://www.loom.com/share/2c034bed467046679285fc88f7d94f4b



                     

                     
 

 





        

            
