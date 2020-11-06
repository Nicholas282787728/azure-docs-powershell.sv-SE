---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573280"
---
# <span data-ttu-id="723c0-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="723c0-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="723c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="723c0-102">SYNOPSIS</span></span>
<span data-ttu-id="723c0-103">Hämtar en eller flera Server hanterings-gateways.</span><span class="sxs-lookup"><span data-stu-id="723c0-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="723c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="723c0-104">SYNTAX</span></span>

### <span data-ttu-id="723c0-105">Inga parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="723c0-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="723c0-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="723c0-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="723c0-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="723c0-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="723c0-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="723c0-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="723c0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="723c0-109">DESCRIPTION</span></span>
<span data-ttu-id="723c0-110">Cmdleten **Get-AzureRmServerManagementGateway** har en eller flera Azure Server Management gateways.</span><span class="sxs-lookup"><span data-stu-id="723c0-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="723c0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="723c0-111">EXAMPLES</span></span>

### <span data-ttu-id="723c0-112">Exempel 1: Hämta alla gateways i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="723c0-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="723c0-113">Det här kommandot får alla Server Management gateways i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="723c0-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="723c0-114">Exempel 2: skaffa gateways i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="723c0-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="723c0-115">Det här kommandot får alla Server hanterings-gateways som tillhör resurs gruppen "Group001.</span><span class="sxs-lookup"><span data-stu-id="723c0-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="723c0-116">Exempel 3: Hämta alla installerade instanser av en gateway</span><span class="sxs-lookup"><span data-stu-id="723c0-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="723c0-117">Med det här kommandot hämtas alla instanser av en Server Management Gateway som heter Gateway01 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="723c0-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="723c0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="723c0-118">PARAMETERS</span></span>

### <span data-ttu-id="723c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723c0-119">-DefaultProfile</span></span>
<span data-ttu-id="723c0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="723c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723c0-121">-Gateway</span><span class="sxs-lookup"><span data-stu-id="723c0-121">-Gateway</span></span>
<span data-ttu-id="723c0-122">Anger en gateway som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="723c0-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="723c0-123">Cmdleten använder parametrarna *ResourceGroupName* och *GatewayName* via angiven Gateway för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="723c0-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="723c0-124">När den här parametern anges inkluderar denna cmdlet detaljerad status för gatewayen.</span><span class="sxs-lookup"><span data-stu-id="723c0-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="723c0-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="723c0-125">-GatewayName</span></span>
<span data-ttu-id="723c0-126">Anger namnet på den server hanterings gateway som denna cmdlet hämtar porten för.</span><span class="sxs-lookup"><span data-stu-id="723c0-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="723c0-127">När du anger parametern *GatewayName* innehåller denna cmdlet detaljerad status för gatewayen.</span><span class="sxs-lookup"><span data-stu-id="723c0-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="723c0-129">Anger namnet på den resurs grupp som cmdleten ska anslutas till.</span><span class="sxs-lookup"><span data-stu-id="723c0-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723c0-130">CommonParameters</span></span>
<span data-ttu-id="723c0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723c0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723c0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723c0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="723c0-133">INPUTS</span></span>

### <span data-ttu-id="723c0-134">Portar</span><span class="sxs-lookup"><span data-stu-id="723c0-134">Gateway</span></span>
<span data-ttu-id="723c0-135">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="723c0-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="723c0-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="723c0-136">OUTPUTS</span></span>

### <span data-ttu-id="723c0-137">Microsoft. Azure. commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="723c0-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="723c0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="723c0-138">NOTES</span></span>
* <span data-ttu-id="723c0-139">Om den här cmdleten används utan parametrar returneras alla gateways som är kopplade till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="723c0-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="723c0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="723c0-140">RELATED LINKS</span></span>

[<span data-ttu-id="723c0-141">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="723c0-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="723c0-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="723c0-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


