---
UID: NF:strmif.IDvdInfo.GetCurrentAudio
title: IDvdInfo::GetCurrentAudio (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the number of available audio streams and the number of the currently selected audio stream.
helpviewer_keywords: ["GetCurrentAudio","GetCurrentAudio method [DirectShow]","GetCurrentAudio method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentAudio method","IDvdInfo.GetCurrentAudio","IDvdInfo::GetCurrentAudio","IDvdInfoGetCurrentAudio","dshow.idvdinfo_getcurrentaudio","strmif/IDvdInfo::GetCurrentAudio"]
old-location: dshow\idvdinfo_getcurrentaudio.htm
tech.root: dshow
ms.assetid: d542e995-3b98-402a-b1d9-253bede7dcff
ms.date: 4/26/2023
ms.keywords: GetCurrentAudio, GetCurrentAudio method [DirectShow], GetCurrentAudio method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentAudio method, IDvdInfo.GetCurrentAudio, IDvdInfo::GetCurrentAudio, IDvdInfoGetCurrentAudio, dshow.idvdinfo_getcurrentaudio, strmif/IDvdInfo::GetCurrentAudio
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo::GetCurrentAudio
 - strmif/IDvdInfo::GetCurrentAudio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetCurrentAudio
---

# IDvdInfo::GetCurrentAudio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the number of available audio streams and the number of the currently selected audio stream.

## -parameters

### -param pulStreamsAvailable [out]

Pointer to the retrieved number of available audio streams

### -param pulCurrentStream [out]

Pointer to the current stream number.

## -returns

Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>