---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577867"
---
# <span data-ttu-id="fdeb8-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="fdeb8-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="fdeb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fdeb8-103">Skaffa en specifik signal tjänst eller alla signal tjänster i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdeb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdeb8-104">SYNTAX</span></span>

### <span data-ttu-id="fdeb8-105">ListSignalRServiceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fdeb8-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdeb8-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdeb8-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdeb8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdeb8-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdeb8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdeb8-108">DESCRIPTION</span></span>
<span data-ttu-id="fdeb8-109">Skaffa en specifik signal tjänst eller alla signal tjänster i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="fdeb8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdeb8-110">EXAMPLES</span></span>

### <span data-ttu-id="fdeb8-111">Hämta alla signal tjänster i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="fdeb8-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="fdeb8-112">Hämta alla signal tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="fdeb8-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="fdeb8-113">Skaffa en specifik signal tjänst</span><span class="sxs-lookup"><span data-stu-id="fdeb8-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="fdeb8-114">Skaffa en specifik signal tjänst från standard resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fdeb8-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="fdeb8-115">Standard resurs gruppen kan anges av `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="fdeb8-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="fdeb8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdeb8-116">PARAMETERS</span></span>

### <span data-ttu-id="fdeb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdeb8-117">-DefaultProfile</span></span>
<span data-ttu-id="fdeb8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdeb8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdeb8-119">-Name</span></span>
<span data-ttu-id="fdeb8-120">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdeb8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdeb8-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdeb8-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdeb8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdeb8-123">-ResourceId</span></span>
<span data-ttu-id="fdeb8-124">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdeb8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdeb8-125">CommonParameters</span></span>
<span data-ttu-id="fdeb8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdeb8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdeb8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdeb8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdeb8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdeb8-128">INPUTS</span></span>

### <span data-ttu-id="fdeb8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fdeb8-129">System.String</span></span>
<span data-ttu-id="fdeb8-130">Parametrar: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdeb8-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="fdeb8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdeb8-131">OUTPUTS</span></span>

### <span data-ttu-id="fdeb8-132">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="fdeb8-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="fdeb8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdeb8-133">NOTES</span></span>

## <span data-ttu-id="fdeb8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdeb8-134">RELATED LINKS</span></span>
