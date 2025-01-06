Custom cv modules must be located on a folder, inside the "custom_cv" folder, inside the root Playful Plugins folder.

"process_names": a list of string used to check if the desired process is being focused and detection should occur, the name of the process must only include one of the values in the list, not match it perfectly (a browser playing the video named "PowerWash Simulator Longplay Full Game Walkthrough" would be detected if "PowerWash" is on the list)

"aspect_ratios": a dict<int, dict> defining the supported aspect ratios

"templates": defines the templates to be used in the computer vision "match template" method, with the template image file to be located in the module folder and it's detection threshold value. For more information see: https://docs.opencv.org/4.x/d4/dc6/tutorial_py_template_matching.html

"regions": defines the regions where detections can occur, should be as small as possible to improve performance. Each region is defined once per aspect ratio (format: sample_w + "x" + sample_h)

"events": defines the events to be detected. each event with a template match operation that triggers its detection

"default_config": the default values to be used when initializing the user's config file for this module