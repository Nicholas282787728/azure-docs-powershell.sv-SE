---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755944"
---
# <span data-ttu-id="952df-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="952df-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="952df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="952df-102">SYNOPSIS</span></span>
<span data-ttu-id="952df-103">Hämta åtkomst nycklar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="952df-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="952df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="952df-104">SYNTAX</span></span>

### <span data-ttu-id="952df-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="952df-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="952df-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="952df-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="952df-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="952df-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="952df-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="952df-108">DESCRIPTION</span></span>
<span data-ttu-id="952df-109">Hämta åtkomst nycklar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="952df-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="952df-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="952df-110">EXAMPLES</span></span>

### <span data-ttu-id="952df-111">Skaffa åtkomst nycklar för en viss signal tjänst</span><span class="sxs-lookup"><span data-stu-id="952df-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="952df-112">Få åtkomst nycklar från ett objekt i en signal tjänst i en pipe</span><span class="sxs-lookup"><span data-stu-id="952df-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="952df-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="952df-113">PARAMETERS</span></span>

### <span data-ttu-id="952df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952df-114">-DefaultProfile</span></span>
<span data-ttu-id="952df-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="952df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="952df-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="952df-116">-InputObject</span></span>
<span data-ttu-id="952df-117">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="952df-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="952df-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="952df-118">-Name</span></span>
<span data-ttu-id="952df-119">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="952df-119">SignalR service name.</span></span>

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

### <span data-ttu-id="952df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952df-120">-ResourceGroupName</span></span>
<span data-ttu-id="952df-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="952df-121">Resource group name.</span></span>

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

### <span data-ttu-id="952df-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="952df-122">-ResourceId</span></span>
<span data-ttu-id="952df-123">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="952df-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="952df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952df-124">CommonParameters</span></span>
<span data-ttu-id="952df-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952df-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952df-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="952df-127">INPUTS</span></span>

### <span data-ttu-id="952df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="952df-128">System.String</span></span>
<span data-ttu-id="952df-129">Parametrar: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="952df-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="952df-130">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="952df-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="952df-131">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="952df-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="952df-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="952df-132">OUTPUTS</span></span>

### <span data-ttu-id="952df-133">Microsoft. Azure. commands. signaler. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="952df-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="952df-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="952df-134">NOTES</span></span>

## <span data-ttu-id="952df-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="952df-135">RELATED LINKS</span></span>
