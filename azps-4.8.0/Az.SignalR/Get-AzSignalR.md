---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261673"
---
# <span data-ttu-id="dfa3e-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="dfa3e-101">Get-AzSignalR</span></span>

## <span data-ttu-id="dfa3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa3e-103">Skaffa en specifik signal tjänst eller alla signal tjänster i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="dfa3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfa3e-104">SYNTAX</span></span>

### <span data-ttu-id="dfa3e-105">ListSignalRServiceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dfa3e-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfa3e-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfa3e-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfa3e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfa3e-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa3e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfa3e-108">DESCRIPTION</span></span>
<span data-ttu-id="dfa3e-109">Skaffa en specifik signal tjänst eller alla signal tjänster i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="dfa3e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfa3e-110">EXAMPLES</span></span>

### <span data-ttu-id="dfa3e-111">Hämta alla signal tjänster i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="dfa3e-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="dfa3e-112">Hämta alla signal tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dfa3e-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="dfa3e-113">Skaffa en specifik signal tjänst</span><span class="sxs-lookup"><span data-stu-id="dfa3e-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="dfa3e-114">Skaffa en specifik signal tjänst från standard resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="dfa3e-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="dfa3e-115">Standard resurs gruppen kan anges via \` set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="dfa3e-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="dfa3e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfa3e-116">PARAMETERS</span></span>

### <span data-ttu-id="dfa3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa3e-117">-DefaultProfile</span></span>
<span data-ttu-id="dfa3e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa3e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfa3e-119">-Name</span></span>
<span data-ttu-id="dfa3e-120">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-120">SignalR service name.</span></span>

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

### <span data-ttu-id="dfa3e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa3e-121">-ResourceGroupName</span></span>
<span data-ttu-id="dfa3e-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-122">Resource group name.</span></span>

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

### <span data-ttu-id="dfa3e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfa3e-123">-ResourceId</span></span>
<span data-ttu-id="dfa3e-124">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="dfa3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa3e-125">CommonParameters</span></span>
<span data-ttu-id="dfa3e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa3e-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfa3e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa3e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfa3e-128">INPUTS</span></span>

### <span data-ttu-id="dfa3e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dfa3e-129">System.String</span></span>
## <span data-ttu-id="dfa3e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfa3e-130">OUTPUTS</span></span>

### <span data-ttu-id="dfa3e-131">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="dfa3e-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="dfa3e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfa3e-132">NOTES</span></span>

## <span data-ttu-id="dfa3e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfa3e-133">RELATED LINKS</span></span>