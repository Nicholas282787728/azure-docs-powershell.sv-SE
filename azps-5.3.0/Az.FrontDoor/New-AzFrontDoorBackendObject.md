---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523661"
---
# <span data-ttu-id="5bd84-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="5bd84-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="5bd84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bd84-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd84-103">Skapa ett PSBackend-objekt</span><span class="sxs-lookup"><span data-stu-id="5bd84-103">Create a PSBackend object</span></span>

## <span data-ttu-id="5bd84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bd84-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bd84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bd84-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd84-106">Skapa ett PSBackend-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5bd84-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="5bd84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bd84-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd84-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5bd84-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="5bd84-109">Skapa ett PSBackend-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5bd84-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="5bd84-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bd84-110">PARAMETERS</span></span>

### <span data-ttu-id="5bd84-111">-Adress</span><span class="sxs-lookup"><span data-stu-id="5bd84-111">-Address</span></span>
<span data-ttu-id="5bd84-112">Plats för Server delen (IP-adress eller FQDN)</span><span class="sxs-lookup"><span data-stu-id="5bd84-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="5bd84-113">-BackendHostHeader</span></span>
<span data-ttu-id="5bd84-114">Det värde som ska användas som värd huvud skickat till Server delen.</span><span class="sxs-lookup"><span data-stu-id="5bd84-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="5bd84-115">Standardvärdet är Server delens adress.</span><span class="sxs-lookup"><span data-stu-id="5bd84-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd84-116">-DefaultProfile</span></span>
<span data-ttu-id="5bd84-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd84-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5bd84-118">-EnabledState</span></span>
<span data-ttu-id="5bd84-119">Om du vill aktivera användning av den här server delen.</span><span class="sxs-lookup"><span data-stu-id="5bd84-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="5bd84-120">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="5bd84-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5bd84-121">-HttpPort</span></span>
<span data-ttu-id="5bd84-122">HTTP TCP-portnumret.</span><span class="sxs-lookup"><span data-stu-id="5bd84-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="5bd84-123">Måste vara mellan 1 och 65535.</span><span class="sxs-lookup"><span data-stu-id="5bd84-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="5bd84-124">Standardvärdet är 80.</span><span class="sxs-lookup"><span data-stu-id="5bd84-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5bd84-125">-HttpsPort</span></span>
<span data-ttu-id="5bd84-126">HTTPS TCP-portnumret.</span><span class="sxs-lookup"><span data-stu-id="5bd84-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="5bd84-127">Måste vara mellan 1 och 65535.</span><span class="sxs-lookup"><span data-stu-id="5bd84-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="5bd84-128">Standardvärdet är 443</span><span class="sxs-lookup"><span data-stu-id="5bd84-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-129">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="5bd84-129">-Priority</span></span>
<span data-ttu-id="5bd84-130">Prioritetsordning för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5bd84-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="5bd84-131">Måste vara mellan 1 och 5.</span><span class="sxs-lookup"><span data-stu-id="5bd84-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="5bd84-132">Standardvärdet är 1</span><span class="sxs-lookup"><span data-stu-id="5bd84-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="5bd84-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="5bd84-134">Alias för den privata länk resursen.</span><span class="sxs-lookup"><span data-stu-id="5bd84-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="5bd84-135">Fyller i det här valfria fältet betyder det att den här server delen är "privat"</span><span class="sxs-lookup"><span data-stu-id="5bd84-135">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="5bd84-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="5bd84-137">Ett anpassat meddelande som ska ingå i godkännandebegäran för att ansluta till den privata länken</span><span class="sxs-lookup"><span data-stu-id="5bd84-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="5bd84-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="5bd84-139">Platsen för den privata länk resursen.</span><span class="sxs-lookup"><span data-stu-id="5bd84-139">The Location of Private Link resource.</span></span> <span data-ttu-id="5bd84-140">Plats krävs när PrivateLinkResourceId är inställt</span><span class="sxs-lookup"><span data-stu-id="5bd84-140">Location is required when PrivateLinkResourceId is set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="5bd84-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5bd84-142">Resurs-ID för den privata länken.</span><span class="sxs-lookup"><span data-stu-id="5bd84-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="5bd84-143">Fyller i det här valfria fältet betyder det att den här server delen är "privat"</span><span class="sxs-lookup"><span data-stu-id="5bd84-143">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-144">-Vikt</span><span class="sxs-lookup"><span data-stu-id="5bd84-144">-Weight</span></span>
<span data-ttu-id="5bd84-145">Slut punktens vikt för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5bd84-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="5bd84-146">Måste vara mellan 1 och 1000.</span><span class="sxs-lookup"><span data-stu-id="5bd84-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="5bd84-147">Standardvärdet är 50</span><span class="sxs-lookup"><span data-stu-id="5bd84-147">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd84-148">CommonParameters</span></span>
<span data-ttu-id="5bd84-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd84-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd84-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bd84-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd84-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bd84-151">INPUTS</span></span>

### <span data-ttu-id="5bd84-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="5bd84-152">None</span></span>

## <span data-ttu-id="5bd84-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bd84-153">OUTPUTS</span></span>

### <span data-ttu-id="5bd84-154">Microsoft. Azure. commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="5bd84-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="5bd84-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bd84-155">NOTES</span></span>

## <span data-ttu-id="5bd84-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bd84-156">RELATED LINKS</span></span>

[<span data-ttu-id="5bd84-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="5bd84-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
