---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099456"
---
# <span data-ttu-id="14a5f-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="14a5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="14a5f-103">Skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="14a5f-103">Creates an application gateway.</span></span>

## <span data-ttu-id="14a5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14a5f-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14a5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="14a5f-106">Cmdleten **New-AzureApplicationGateway** skapar en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="14a5f-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="14a5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14a5f-107">EXAMPLES</span></span>

### <span data-ttu-id="14a5f-108">Exempel 1: skapa en Programgateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="14a5f-109">Det här kommandot skapar en Programgateway som heter ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="14a5f-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="14a5f-110">Kommandot distribuerar gatewayen i VirtualNetwork17 och i de angivna under näten.</span><span class="sxs-lookup"><span data-stu-id="14a5f-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="14a5f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14a5f-111">PARAMETERS</span></span>

### <span data-ttu-id="14a5f-112">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="14a5f-112">-Description</span></span>
<span data-ttu-id="14a5f-113">Anger en beskrivning av att denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="14a5f-114">-GatewaySize</span></span>
<span data-ttu-id="14a5f-115">Anger den storlek som denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="14a5f-116">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="14a5f-116">Valid values are:</span></span>

- <span data-ttu-id="14a5f-117">Eld</span><span class="sxs-lookup"><span data-stu-id="14a5f-117">Small</span></span>
- <span data-ttu-id="14a5f-118">Risk</span><span class="sxs-lookup"><span data-stu-id="14a5f-118">Medium</span></span>
- <span data-ttu-id="14a5f-119">Höga</span><span class="sxs-lookup"><span data-stu-id="14a5f-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="14a5f-120">-InstanceCount</span></span>
<span data-ttu-id="14a5f-121">Anger antalet instanser som denna cmdlet tilldelar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="14a5f-122">-Name</span></span>
<span data-ttu-id="14a5f-123">Anger ett namn för den nya programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="14a5f-124">-Profile</span></span>
<span data-ttu-id="14a5f-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="14a5f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14a5f-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-127">-Undernät</span><span class="sxs-lookup"><span data-stu-id="14a5f-127">-Subnets</span></span>
<span data-ttu-id="14a5f-128">Anger en matris med undernät där denna cmdlet distribuerar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="14a5f-129">-VnetName</span></span>
<span data-ttu-id="14a5f-130">Anger det virtuella nätverk där denna cmdlet distribuerar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14a5f-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a5f-131">CommonParameters</span></span>
<span data-ttu-id="14a5f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a5f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a5f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a5f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14a5f-134">INPUTS</span></span>

### <span data-ttu-id="14a5f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14a5f-135">System.String</span></span>

## <span data-ttu-id="14a5f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14a5f-136">OUTPUTS</span></span>

### <span data-ttu-id="14a5f-137">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="14a5f-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="14a5f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14a5f-138">NOTES</span></span>

## <span data-ttu-id="14a5f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14a5f-139">RELATED LINKS</span></span>

[<span data-ttu-id="14a5f-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="14a5f-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="14a5f-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="14a5f-143">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="14a5f-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14a5f-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
