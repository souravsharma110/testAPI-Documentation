# Mappls Sessions Tags Management

Tags in Session Tracking are essentially code snippets that allow you to track various types of user behavior on your website, such as clicks, form submissions, or pageviews. When a particular trigger is fired, the corresponding tag is activated, and the data is sent to the analytics tool you have set up, such as Google Analytics.

Triggers in Session Tracking determine when a tag should be fired. You can set up triggers based on a range of user actions, such as clicks, pageviews, or form submissions. For example, you can create a trigger that fires a tag when a user clicks on a particular button or visits a specific page.

When you set up a tag in Session Tracking, you also set up a corresponding trigger that tells the tag when to fire. You can create multiple triggers for a single tag, depending on the specific user behavior you want to track.

By using tags and triggers in Session Tracking, you can track a wide range of user behavior on your website, and gain insights into how users interact with your content. This can help you make data-driven decisions about how to improve your website's user experience and achieve your business goals.

## How this things works

- **Installation**: The first step in using a tag management tool is to install the tag management container on your website. The container is a piece of JavaScript code that allows the tag management tool to interact with your website.

- **Configuration**: Once the tag management container is installed on your website, you can start configuring your tags and triggers in the tag management tool's interface. This involves setting up the tags that you want to fire when a particular trigger is activated, and specifying the rules that determine when a trigger should be activated.

- **Data collection**: When a user interacts with your website, the tag management container on your website sends data to the tag management tool's backend system. The backend system processes this data and determines which tags should be fired based on the triggers you have set up.

- **Tag firing**: When a tag is fired, the tag management container on your website sends a request to the corresponding analytics or marketing tool. This tool then processes the data and updates your analytics or advertising reports.

- **Reporting**: Finally, the tag management tool's backend system collects all of the data from the tags and triggers, and provides reporting and analysis features that allow you to understand how users are interacting with your website, and optimize your marketing and user experience strategies accordingly.

```
            +----------------------------------+
            |                                  |
            |     Website with Tag Container   |
            |                                  |
            +-----------------+----------------+
                              |
                +-------------+-------------+
                |                           |
       +--------+--------+        +---------+---------+
       |  Rules Engine   |        |    Tag Library    |
       +-----------------+        +---------+---------+
                                            |
                             +--------------+---------------+
                             |              |               |
                       +-----+-----+  +-----+-----+  +--------+--------+
                       | Custom Tag |  | Custom Tag |  |  Pre-built Tag  |
                       +-----------+  +-----------+  +-----------------+
                                            |
                                      +-----+-----+
                                      | Data Layer |
                                      +-----------+
                                            |
                             +--------------+---------------+
                             |                              |
                      +-----+-----+                +---------+---------+
                      | Analytics |                |     Reporting     |
                      +-----------+                +-------------------+
```

## API Needed

### Create Session Account

### Create Container

### Get All Variable Types

```json
{
    "default": {
        "builtInVariableType": [
            {
                "name": "Page URL",
                "type": 1,
                "publicId": "u"
            },
            {
                "name": "Page Hostname",
                "type": 2,
                "publicId": "u"
            },
            {
                "name": "Page Path",
                "type": 3,
                "publicId": "u"
            },
            {
                "name": "Referrer",
                "type": 4,
                "publicId": "f"
            },
            {
                "name": "Event",
                "type": 5,
                "publicId": "e"
            },
            {
                "name": "Click Element",
                "type": 6,
                "publicId": "v"
            },
            {
                "name": "Click Classes",
                "type": 7,
                "publicId": "v"
            },
            {
                "name": "Click ID",
                "type": 8,
                "publicId": "v"
            },
            {
                "name": "Click Target",
                "type": 9,
                "publicId": "v"
            },
            {
                "name": "Click URL",
                "type": 10,
                "publicId": "v"
            },
            {
                "name": "Click Text",
                "type": 11,
                "publicId": "aev"
            },
            {
                "name": "Form Element",
                "type": 12,
                "publicId": "v"
            },
            {
                "name": "Form Classes",
                "type": 13,
                "publicId": "v"
            },
            {
                "name": "Form ID",
                "type": 14,
                "publicId": "v"
            },
            {
                "name": "Form Target",
                "type": 15,
                "publicId": "v"
            },
            {
                "name": "Form URL",
                "type": 16,
                "publicId": "v"
            },
            {
                "name": "Form Text",
                "type": 17,
                "publicId": "aev"
            },
            {
                "name": "Error Message",
                "type": 18,
                "publicId": "v"
            },
            {
                "name": "Error URL",
                "type": 19,
                "publicId": "v"
            },
            {
                "name": "Error Line",
                "type": 20,
                "publicId": "v"
            },
            {
                "name": "New History Fragment",
                "type": 21,
                "publicId": "v"
            },
            {
                "name": "Old History Fragment",
                "type": 22,
                "publicId": "v"
            },
            {
                "name": "New History State",
                "type": 23,
                "publicId": "v"
            },
            {
                "name": "Old History State",
                "type": 24,
                "publicId": "v"
            },
            {
                "name": "History Source",
                "type": 25,
                "publicId": "v"
            },
            {
                "name": "HTML ID",
                "type": 46,
                "publicId": "hid"
            },
            {
                "name": "Container Version",
                "type": 26,
                "publicId": "ctv"
            },
            {
                "name": "Debug Mode",
                "type": 27,
                "publicId": "dbg"
            },
            {
                "name": "Random Number",
                "type": 28,
                "publicId": "r"
            },
            {
                "name": "Container ID",
                "type": 29,
                "publicId": "cid"
            },
            {
                "name": "Environment Name",
                "type": 54,
                "publicId": "ev"
            },
            {
                "name": "Video Provider",
                "type": 105,
                "publicId": "v"
            },
            {
                "name": "Video URL",
                "type": 106,
                "publicId": "v"
            },
            {
                "name": "Video Title",
                "type": 107,
                "publicId": "v"
            },
            {
                "name": "Video Duration",
                "type": 108,
                "publicId": "v"
            },
            {
                "name": "Video Percent",
                "type": 110,
                "publicId": "v"
            },
            {
                "name": "Video Visible",
                "type": 111,
                "publicId": "v"
            },
            {
                "name": "Video Status",
                "type": 112,
                "publicId": "v"
            },
            {
                "name": "Video Current Time",
                "type": 113,
                "publicId": "v"
            },
            {
                "name": "Scroll Depth Threshold",
                "type": 114,
                "publicId": "v"
            },
            {
                "name": "Scroll Depth Units",
                "type": 115,
                "publicId": "v"
            },
            {
                "name": "Scroll Direction",
                "type": 116,
                "publicId": "v"
            },
            {
                "name": "Percent Visible",
                "type": 117,
                "publicId": "v"
            },
            {
                "name": "On-Screen Duration",
                "type": 118,
                "publicId": "v"
            },
            {
                "name": "First Time Visible",
                "type": 119,
                "publicId": "v"
            },
            {
                "name": "Last Time Visible",
                "type": 120,
                "publicId": "v"
            }
        ]
    }
}
```

### Create New Tag

`Method Type`: POST

`Request URL`: https://sessions.mappls.com/api/accounts/{accountId}/containers/{containerId}/workspaces/{workspaceId}/tags

`Request Body:`

```json

```

### Create Trigger

`Method Type`: POST

`Request URL`: https://sessions.mappls.com/api/accounts/{accountId}/containers/{containerId}/workspaces/{workspaceId}/triggers

`Request Body:`

```json
{
    "data": {
        "name": "test-1",
        "filter": [
            {
                "operator": "CONTAINS",
                "arg": [
                    {
                        "type": 4,
                        "macroReference": "Click Classes"
                    },
                    {
                        "type": 1,
                        "string": "arrow_drop_down"
                    }
                ],
                "negate": false,
                "type": 4
            }
        ],
        "customEventFilter": [],
        "autoEventFilter": [],
        "type": 7
    }
}
```

### Update Triggers

`Request Body`

```json
{
    "key": {
        "accountId": "137018856",
        "containerId": "53004360",
        "triggerId": 31,
        "containerDraftId": 4
    },
    "data": {
        "name": "test-1",
        "type": 7,
        "customEventFilter": [],
        "filter": [
            {
                "type": 4,
                "negate": false,
                "arg": [
                    {
                        "type": 4,
                        "listItem": [],
                        "mapKey": [],
                        "mapValue": [],
                        "macroReference": "Click Classes",
                        "templateToken": [],
                        "escaping": []
                    },
                    {
                        "type": 1,
                        "string": "arrow_drop_down",
                        "listItem": [],
                        "mapKey": [],
                        "mapValue": [],
                        "templateToken": [],
                        "escaping": []
                    }
                ],
                "operator": "CONTAINS"
            },
            {
                "operator": "CONTAINS",
                "arg": [
                    {
                        "type": 4,
                        "macroReference": "Click Classes"
                    },
                    {
                        "type": 1,
                        "string": "arrow_up"
                    }
                ],
                "negate": false,
                "type": 4
            }
        ],
        "autoEventFilter": [],
        "clickListener": {},
        "typeDisplayName": "All Elements"
    },
    "statMetadata": {
        "createdTime": "1676978299582",
        "modifiedTime": "1676978299582",
        "entityVersion": "1676978299582"
    },
    "isBuiltIn": false,
    "containerDraftMetadata": {
        "changeStatus": 1
    },
    "references": []
}
```

### Get Container Details

Example Response of Google Container Details

```json
{
"default": {
"key": {
    "accountId": "137018856",
    "containerId": "53004360"
},
"data": {
    "name": "MapmyIndia API Console",
    "domainName": [],
    "publicId": "GTM-TQ9HJLZ",
    "aliases": [
        "GTM-TQ9HJLZ"
    ],
    "timeZoneId": 1,
    "timeZoneCountryCode": "US",
    "usageContext": [
        0
    ],
    "allowlists": {},
    "enabledBuiltInMacro": [
        6,
        7,
        8,
        9,
        10,
        11,
        1,
        2,
        3,
        4,
        5
    ],
    "experimentInfo": [],
    "securitySettings": {},
    "denormalizedLinks": []
},
"status": {
    "publishedVersionId": 3,
    "highestVersionId": 3,
    "defaultContainerDraftId": 4,
    "containerDraftsReady": true,
    "entitiesFlaggedForMalware": []
},
"statMetadata": {
    "createdTime": "1634192773879",
    "modifiedTime": "1634192773879",
    "entityVersion": "1634192773879"
},
"pendingApprovalCount": 0
}
}
```

### Get All Trigger Type Events

Example Response of Google Trigger Type Events

```json
{
"default": {
"eventType": [
    {
        "key": 36,
        "displayName": "Initialization",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All Initialization Events",
        "groupDisplayNameSomeEvents": "Some Initialization Events",
        "context": [
            0
        ]
    },
    {
        "key": 38,
        "displayName": "Consent Initialization",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            0
        ]
    },
    {
        "key": 1,
        "displayName": "Page View",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All Page Views",
        "groupDisplayNameSomeEvents": "Some Page Views",
        "context": [
            5,
            0
        ]
    },
    {
        "key": 39,
        "displayName": "Page View",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All Page Views",
        "groupDisplayNameSomeEvents": "Some Page Views",
        "context": [
            7
        ]
    },
    {
        "key": 2,
        "displayName": "DOM Ready",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All DOM Ready Events",
        "groupDisplayNameSomeEvents": "Some DOM Ready Events",
        "context": [
            0
        ]
    },
    {
        "key": 3,
        "displayName": "Window Loaded",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Page View",
        "groupDisplayNameAllEvents": "All Window Loaded Events",
        "groupDisplayNameSomeEvents": "Some Window Loaded Events",
        "context": [
            0
        ]
    },
    {
        "key": 3,
        "displayName": "Container Loaded",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All Container Loaded Events",
        "groupDisplayNameSomeEvents": "Some Container Loaded Events",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 7,
        "displayName": "All Elements",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Click",
        "groupDisplayNameAllEvents": "All Clicks",
        "groupDisplayNameSomeEvents": "Some Clicks",
        "context": [
            0
        ]
    },
    {
        "key": 8,
        "displayName": "Just Links",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Click",
        "groupDisplayNameAllEvents": "All Link Clicks",
        "groupDisplayNameSomeEvents": "Some Link Clicks",
        "context": [
            0
        ]
    },
    {
        "key": 6,
        "displayName": "Form Submission",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "User Engagement",
        "groupDisplayNameAllEvents": "All Forms",
        "groupDisplayNameSomeEvents": "Some Forms",
        "context": [
            0
        ]
    },
    {
        "key": 31,
        "displayName": "Scroll Depth",
        "vendorTemplatePublicId": "sdl",
        "groupDisplayName": "User Engagement",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            0
        ]
    },
    {
        "key": 32,
        "displayName": "Element Visibility",
        "vendorTemplatePublicId": "evl",
        "groupDisplayName": "User Engagement",
        "groupDisplayNameAllEvents": "All Visibility Events",
        "groupDisplayNameSomeEvents": "Some Visibility Events",
        "context": [
            0
        ]
    },
    {
        "key": 10,
        "displayName": "History Change",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All History Changes",
        "groupDisplayNameSomeEvents": "Some History Changes",
        "context": [
            0
        ]
    },
    {
        "key": 4,
        "displayName": "Custom Event",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All Custom Events",
        "groupDisplayNameSomeEvents": "Some Custom Events",
        "context": [
            0,
            7
        ]
    },
    {
        "key": 9,
        "displayName": "JavaScript Error",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All JavaScript Errors",
        "groupDisplayNameSomeEvents": "Some JavaScript Errors",
        "context": [
            0
        ]
    },
    {
        "key": 12,
        "displayName": "Timer",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All Timers",
        "groupDisplayNameSomeEvents": "Some Timers",
        "context": [
            0
        ]
    },
    {
        "key": 30,
        "displayName": "YouTube Video",
        "vendorTemplatePublicId": "ytl",
        "groupDisplayName": "User Engagement",
        "groupDisplayNameAllEvents": "All Videos",
        "groupDisplayNameSomeEvents": "Some Videos",
        "context": [
            0
        ]
    },
    {
        "key": 33,
        "displayName": "Trigger Group",
        "vendorTemplatePublicId": "tg",
        "groupDisplayName": "Other",
        "groupDisplayNameAllEvents": "All Conditions",
        "groupDisplayNameSomeEvents": "Some Conditions",
        "context": [
            0
        ]
    },
    {
        "key": 14,
        "displayName": "Click",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Click",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            5
        ]
    },
    {
        "key": 15,
        "displayName": "Timer",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Timer",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            5
        ]
    },
    {
        "key": 16,
        "displayName": "Scroll",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Scroll",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            5
        ]
    },
    {
        "key": 17,
        "displayName": "Visibility",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Visibility",
        "groupDisplayNameAllEvents": "All Pages",
        "groupDisplayNameSomeEvents": "Some Pages",
        "context": [
            5
        ]
    },
    {
        "key": 5,
        "displayName": "Custom",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Custom",
        "groupDisplayNameAllEvents": "All Events",
        "groupDisplayNameSomeEvents": "Some Events",
        "context": [
            1,
            3,
            2,
            4,
            7
        ]
    },
    {
        "key": 18,
        "displayName": "App Exception",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All App Exceptions",
        "groupDisplayNameSomeEvents": "Some App Exceptions",
        "context": [
            3
        ]
    },
    {
        "key": 19,
        "displayName": "App Update",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All App Updates",
        "groupDisplayNameSomeEvents": "Some App Updates",
        "context": [
            4
        ]
    },
    {
        "key": 20,
        "displayName": "Campaign",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Campaigns",
        "groupDisplayNameSomeEvents": "Some Campaigns",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 21,
        "displayName": "First Open",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All First Opens",
        "groupDisplayNameSomeEvents": "Some First Opens",
        "context": [
            4
        ]
    },
    {
        "key": 22,
        "displayName": "In-App Purchase",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All In-App Purchases",
        "groupDisplayNameSomeEvents": "Some In-App Purchases",
        "context": [
            4
        ]
    },
    {
        "key": 23,
        "displayName": "Notification Dismiss",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Notification Dismiss events",
        "groupDisplayNameSomeEvents": "Some Notification Dismiss events",
        "context": [
            3
        ]
    },
    {
        "key": 24,
        "displayName": "Notification Foreground",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Notification Foreground events",
        "groupDisplayNameSomeEvents": "Some Notification Foreground events",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 25,
        "displayName": "Notification Open",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Notification Open events",
        "groupDisplayNameSomeEvents": "Some Notification Open events",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 26,
        "displayName": "Notification Receive",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Notification Receive events",
        "groupDisplayNameSomeEvents": "Some Notification Receive events",
        "context": [
            3
        ]
    },
    {
        "key": 27,
        "displayName": "OS update",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All OS updates",
        "groupDisplayNameSomeEvents": "Some OS updates",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 28,
        "displayName": "Session Start",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All Session Starts",
        "groupDisplayNameSomeEvents": "Some Session Starts",
        "context": [
            3,
            4
        ]
    },
    {
        "key": 29,
        "displayName": "User Engagement",
        "vendorTemplatePublicId": "",
        "groupDisplayName": "Firebase Automatic Events",
        "groupDisplayNameAllEvents": "All User Engagements",
        "groupDisplayNameSomeEvents": "Some User Engagements",
        "context": [
            3,
            4
        ]
    }
]
}
}
```

### Get All Variables

Example Response of Google Variables

```json
{
"default": {
"variable": [
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481607,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click Element",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "v"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 6,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481608,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click Classes",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "v"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 7,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481609,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click ID",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "v"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 8,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481610,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click Target",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "v"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 9,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481611,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click URL",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "v"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 10,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481612,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click Text",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "aev"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 11,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481602,
            "containerDraftId": 4
        },
        "data": {
            "name": "Page URL",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "u"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 1,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481603,
            "containerDraftId": 4
        },
        "data": {
            "name": "Page Hostname",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "u"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 2,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481604,
            "containerDraftId": 4
        },
        "data": {
            "name": "Page Path",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "u"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 3,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481605,
            "containerDraftId": 4
        },
        "data": {
            "name": "Referrer",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "f"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 4,
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "macroId": 2147481606,
            "containerDraftId": 4
        },
        "data": {
            "name": "Event",
            "type": 41,
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [],
            "negativeTriggerId": [],
            "parentFolderId": 0,
            "vendorTemplate": {
                "key": {
                    "publicId": "e"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "0",
            "modifiedTime": "0",
            "entityVersion": "0"
        },
        "isBuiltIn": true,
        "builtInType": 5,
        "references": []
    }
]
}
}
```

### Get All Tags

Example Response of Google Tags API

```json
{
"default": {
"tag": [
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "tagId": 6,
            "containerDraftId": 4
        },
        "data": {
            "name": "Activated Date",
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [
                5
            ],
            "negativeTriggerId": [],
            "type": 46,
            "parentFolderId": 0,
            "setupTag": [],
            "teardownTag": [],
            "paused": false,
            "consentSettings": {
                "manualConsentStatus": 0,
                "manualConsentSettings": {
                    "type": 2,
                    "listItem": [],
                    "mapKey": [],
                    "mapValue": [],
                    "templateToken": [],
                    "escaping": []
                }
            },
            "vendorTemplate": {
                "key": {
                    "publicId": "gaawe"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "1638855477170",
            "modifiedTime": "1638855477170",
            "entityVersion": "1638855477170"
        },
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "tagId": 17,
            "containerDraftId": 4
        },
        "data": {
            "name": "Allocations",
            "positiveConditionId": [],
            "negativeConditionId": [],
            "positiveTriggerId": [
                7
            ],
            "negativeTriggerId": [],
            "type": 46,
            "parentFolderId": 0,
            "setupTag": [],
            "teardownTag": [],
            "paused": false,
            "consentSettings": {
                "manualConsentStatus": 0,
                "manualConsentSettings": {
                    "type": 2,
                    "listItem": [],
                    "mapKey": [],
                    "mapValue": [],
                    "templateToken": [],
                    "escaping": []
                }
            },
            "vendorTemplate": {
                "key": {
                    "publicId": "gaawe"
                },
                "param": [],
                "valueCache": []
            }
        },
        "statMetadata": {
            "createdTime": "1638860465123",
            "modifiedTime": "1638860465123",
            "entityVersion": "1638860465123"
        },
        "references": []
    },
]
}
}
```

### Get All Triggers

Example response of Google Triggers API

```json
{
"default": {
"trigger": [
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "triggerId": 29,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click Logo",
            "type": 7,
            "customEventFilter": [],
            "filter": [
                {
                    "type": 4,
                    "negate": false,
                    "arg": [
                        {
                            "type": 4,
                            "listItem": [],
                            "mapKey": [],
                            "mapValue": [],
                            "macroReference": "Click URL",
                            "templateToken": [],
                            "escaping": []
                        },
                        {
                            "type": 1,
                            "string": "https://apis.mappls.com/console/assets/mmi_logo_new.svg",
                            "listItem": [],
                            "mapKey": [],
                            "mapValue": [],
                            "templateToken": [],
                            "escaping": []
                        }
                    ]
                },
                {
                    "type": 4,
                    "negate": false,
                    "arg": [
                        {
                            "type": 4,
                            "listItem": [],
                            "mapKey": [],
                            "mapValue": [],
                            "macroReference": "Click Classes",
                            "templateToken": [],
                            "escaping": []
                        },
                        {
                            "type": 1,
                            "string": "Sourav Sharma",
                            "listItem": [],
                            "mapKey": [],
                            "mapValue": [],
                            "templateToken": [],
                            "escaping": []
                        }
                    ]
                }
            ],
            "autoEventFilter": [],
            "clickListener": {}
        },
        "statMetadata": {
            "createdTime": "1676889885430",
            "modifiedTime": "1676890780713",
            "entityVersion": "1676890780713"
        },
        "isBuiltIn": false,
        "containerDraftMetadata": {
            "changeStatus": 0
        },
        "references": []
    },
    {
        "key": {
            "accountId": "137018856",
            "containerId": "53004360",
            "triggerId": 4,
            "containerDraftId": 4
        },
        "data": {
            "name": "Click",
            "type": 7,
            "customEventFilter": [],
            "filter": [],
            "autoEventFilter": [],
            "clickListener": {}
        },
        "statMetadata": {
            "createdTime": "1634193299732",
            "modifiedTime": "1634193299732",
            "entityVersion": "1634193299732"
        },
        "isBuiltIn": false,
        "containerDraftMetadata": {
            "changeStatus": 0
        },
        "references": []
    },
    // rest all the data will come in this format
]
}
}
```


#### URL:
https://anchor.mappls.com/api/pigeon/audiences/

#### Method:
GET

#### Identity Access Management
A grant type of `Password` is mandatory for this request. What we mean by this is, that a user log-in is mandatory.

> `Authorization` Header needs to be passed with the user `access token` (from Outpost `OAuth 2.0`) to authorize the request.

#### Permissions Required:
anchor.pigeon.audiences.read

#### Success Response
- Code : `200 OK`

    Content: A JSON array of recipient lists, where each recipient list has the following properties:

  - `listId`: A unique identifier for the recipient list (integer).
  - `name`: The name of the recipient list (string).
  - `description`: A brief description of the recipient list (string).
  - `recipientCount`: The number of recipients in the list (integer).

  ```json
  [
      {
          "id": aud00021326456,
          "name": "Mappls Android",
          "description": "List of all Mappls Android users",
          "recipient_count": "250000",
          "created":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          },
          "updated":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          }
      },
      {
          "id": aud00021326456,
          "name": "Mappls iOS",
          "description": "List of all Mappls iOS users",
          "recipient_count": "150002",
          "created":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          },
          "updated":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          }
      },
      {
        // rest of the mailing lists
      }
  ]
  ```
- Code: `401 Unauthorized`

    Content:
  ```json
  {
    "error": "Unauthorized access"
  }
  ```
- Code: `403 Forbidden`

    Content:
  ```json
  {
    "error": "Access denied, insufficient permissions"
  }
  ```