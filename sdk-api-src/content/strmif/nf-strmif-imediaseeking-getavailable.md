---
UID: NF:strmif.IMediaSeeking.GetAvailable
title: IMediaSeeking::GetAvailable (strmif.h)
description: The GetAvailable method retrieves the range of times in which seeking is efficient.
helpviewer_keywords: ["GetAvailable","GetAvailable method [DirectShow]","GetAvailable method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetAvailable method","IMediaSeeking.GetAvailable","IMediaSeeking::GetAvailable","IMediaSeekingGetAvailable","dshow.imediaseeking_getavailable","strmif/IMediaSeeking::GetAvailable"]
old-location: dshow\imediaseeking_getavailable.htm
tech.root: dshow
ms.assetid: 8c4114e5-ff82-421a-a7fb-9382d4182388
ms.date: 4/26/2023
ms.keywords: GetAvailable, GetAvailable method [DirectShow], GetAvailable method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetAvailable method, IMediaSeeking.GetAvailable, IMediaSeeking::GetAvailable, IMediaSeekingGetAvailable, dshow.imediaseeking_getavailable, strmif/IMediaSeeking::GetAvailable
req.header: strmif.h
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
 - IMediaSeeking::GetAvailable
 - strmif/IMediaSeeking::GetAvailable
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
 - IMediaSeeking.GetAvailable
---

# IMediaSeeking::GetAvailable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAvailable</code> method retrieves the range of times in which seeking is efficient.

## -parameters

### -param pEarliest [out]

Pointer to a variable that receives the earliest time for efficient seeking.

### -param pLatest [out]

Pointer to a variable that receives the latest time for efficient seeking.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

This method is intended primarily for seeking in media streams that might have excessive latency, such as streams being sent over a network. The returned values indicate cached data that has already arrived, which can be easily seeked. It is assumed that seeking to values beyond these returned parameters will cause a delay while the application waits for the data to arrive.

All time values are expressed in the current time format. The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>