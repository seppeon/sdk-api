---
UID: NF:control.IBasicVideo.put_DestinationLeft
title: IBasicVideo::put_DestinationLeft (control.h)
description: The put_DestinationLeft method sets the x-coordinate of the destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","put_DestinationLeft method","IBasicVideo.put_DestinationLeft","IBasicVideo::put_DestinationLeft","IBasicVideoput_DestinationLeft","control/IBasicVideo::put_DestinationLeft","dshow.ibasicvideo_put_destinationleft","put_DestinationLeft","put_DestinationLeft method [DirectShow]","put_DestinationLeft method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_put_destinationleft.htm
tech.root: dshow
ms.assetid: 718fcc07-1e37-4e37-ab99-39f629e65309
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],put_DestinationLeft method, IBasicVideo.put_DestinationLeft, IBasicVideo::put_DestinationLeft, IBasicVideoput_DestinationLeft, control/IBasicVideo::put_DestinationLeft, dshow.ibasicvideo_put_destinationleft, put_DestinationLeft, put_DestinationLeft method [DirectShow], put_DestinationLeft method [DirectShow],IBasicVideo interface
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicVideo::put_DestinationLeft
 - control/IBasicVideo::put_DestinationLeft
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo.put_DestinationLeft
---

# IBasicVideo::put_DestinationLeft


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_DestinationLeft</code> method sets the x-coordinate of the destination rectangle.

## -parameters

### -param DestinationLeft [in]

Specifies the x-coordinate, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>