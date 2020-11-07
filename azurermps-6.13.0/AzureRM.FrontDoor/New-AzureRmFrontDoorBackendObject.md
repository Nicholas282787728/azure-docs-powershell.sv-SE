---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756163"
---
# <span data-ttu-id="e4122-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="e4122-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="e4122-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4122-102">SYNOPSIS</span></span>
<span data-ttu-id="e4122-103">Skapa ett PSBackend-objekt</span><span class="sxs-lookup"><span data-stu-id="e4122-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4122-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4122-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4122-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4122-105">DESCRIPTION</span></span>
<span data-ttu-id="e4122-106">Skapa ett PSBackend-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="e4122-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e4122-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4122-107">EXAMPLES</span></span>

### <span data-ttu-id="e4122-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e4122-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="e4122-109">Skapa ett PSBackend-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="e4122-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e4122-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4122-110">PARAMETERS</span></span>

### <span data-ttu-id="e4122-111">-Adress</span><span class="sxs-lookup"><span data-stu-id="e4122-111">-Address</span></span>
<span data-ttu-id="e4122-112">Plats för Server delen (IP-adress eller FQDN)</span><span class="sxs-lookup"><span data-stu-id="e4122-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="e4122-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="e4122-113">-BackendHostHeader</span></span>
<span data-ttu-id="e4122-114">Det värde som ska användas som värd huvud skickat till Server delen.</span><span class="sxs-lookup"><span data-stu-id="e4122-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="e4122-115">Standardvärdet är Server delens adress.</span><span class="sxs-lookup"><span data-stu-id="e4122-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="e4122-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4122-116">-DefaultProfile</span></span>
<span data-ttu-id="e4122-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4122-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4122-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e4122-118">-EnabledState</span></span>
<span data-ttu-id="e4122-119">Om du vill aktivera användning av den här server delen.</span><span class="sxs-lookup"><span data-stu-id="e4122-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="e4122-120">Standardvärdet är aktiverat</span><span class="sxs-lookup"><span data-stu-id="e4122-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="e4122-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e4122-121">-HttpPort</span></span>
<span data-ttu-id="e4122-122">HTTP TCP-portnumret.</span><span class="sxs-lookup"><span data-stu-id="e4122-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="e4122-123">Måste vara mellan 1 och 65535.</span><span class="sxs-lookup"><span data-stu-id="e4122-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e4122-124">Standardvärdet är 80.</span><span class="sxs-lookup"><span data-stu-id="e4122-124">Default value is 80.</span></span>

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

### <span data-ttu-id="e4122-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e4122-125">-HttpsPort</span></span>
<span data-ttu-id="e4122-126">HTTPS TCP-portnumret.</span><span class="sxs-lookup"><span data-stu-id="e4122-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="e4122-127">Måste vara mellan 1 och 65535.</span><span class="sxs-lookup"><span data-stu-id="e4122-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e4122-128">Standardvärdet är 443</span><span class="sxs-lookup"><span data-stu-id="e4122-128">Default value is 443</span></span>

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

### <span data-ttu-id="e4122-129">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="e4122-129">-Priority</span></span>
<span data-ttu-id="e4122-130">Prioritetsordning för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e4122-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="e4122-131">Måste vara mellan 1 och 5.</span><span class="sxs-lookup"><span data-stu-id="e4122-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="e4122-132">Standardvärdet är 1</span><span class="sxs-lookup"><span data-stu-id="e4122-132">Default value is 1</span></span>

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

### <span data-ttu-id="e4122-133">-Vikt</span><span class="sxs-lookup"><span data-stu-id="e4122-133">-Weight</span></span>
<span data-ttu-id="e4122-134">Slut punktens vikt för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e4122-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="e4122-135">Måste vara mellan 1 och 1000.</span><span class="sxs-lookup"><span data-stu-id="e4122-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="e4122-136">Standardvärdet är 50</span><span class="sxs-lookup"><span data-stu-id="e4122-136">Default value is 50</span></span>

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

### <span data-ttu-id="e4122-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4122-137">CommonParameters</span></span>
<span data-ttu-id="e4122-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4122-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4122-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4122-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4122-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4122-140">INPUTS</span></span>

### <span data-ttu-id="e4122-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4122-141">None</span></span>

## <span data-ttu-id="e4122-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4122-142">OUTPUTS</span></span>

### <span data-ttu-id="e4122-143">Microsoft. Azure. commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="e4122-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="e4122-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4122-144">NOTES</span></span>

## <span data-ttu-id="e4122-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4122-145">RELATED LINKS</span></span>

[<span data-ttu-id="e4122-146">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e4122-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
