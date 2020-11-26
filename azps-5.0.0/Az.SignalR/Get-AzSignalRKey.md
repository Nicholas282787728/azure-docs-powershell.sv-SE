---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324252"
---
# <span data-ttu-id="42427-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="42427-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="42427-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42427-102">SYNOPSIS</span></span>
<span data-ttu-id="42427-103">Hämta åtkomst nycklar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="42427-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="42427-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42427-104">SYNTAX</span></span>

### <span data-ttu-id="42427-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42427-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42427-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42427-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42427-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42427-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42427-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42427-108">DESCRIPTION</span></span>
<span data-ttu-id="42427-109">Hämta åtkomst nycklar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="42427-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="42427-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42427-110">EXAMPLES</span></span>

### <span data-ttu-id="42427-111">Skaffa åtkomst nycklar för en viss signal tjänst</span><span class="sxs-lookup"><span data-stu-id="42427-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="42427-112">Få åtkomst nycklar från ett objekt i en signal tjänst i en pipe</span><span class="sxs-lookup"><span data-stu-id="42427-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="42427-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42427-113">PARAMETERS</span></span>

### <span data-ttu-id="42427-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42427-114">-DefaultProfile</span></span>
<span data-ttu-id="42427-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42427-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42427-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42427-116">-InputObject</span></span>
<span data-ttu-id="42427-117">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="42427-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42427-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="42427-118">-Name</span></span>
<span data-ttu-id="42427-119">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="42427-119">SignalR service name.</span></span>

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

### <span data-ttu-id="42427-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42427-120">-ResourceGroupName</span></span>
<span data-ttu-id="42427-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="42427-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42427-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42427-122">-ResourceId</span></span>
<span data-ttu-id="42427-123">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="42427-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="42427-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42427-124">CommonParameters</span></span>
<span data-ttu-id="42427-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42427-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42427-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42427-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42427-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42427-127">INPUTS</span></span>

### <span data-ttu-id="42427-128">System. String</span><span class="sxs-lookup"><span data-stu-id="42427-128">System.String</span></span>
### <span data-ttu-id="42427-129">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="42427-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="42427-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42427-130">OUTPUTS</span></span>

### <span data-ttu-id="42427-131">Microsoft. Azure. commands. signaler. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="42427-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="42427-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42427-132">NOTES</span></span>

## <span data-ttu-id="42427-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42427-133">RELATED LINKS</span></span>