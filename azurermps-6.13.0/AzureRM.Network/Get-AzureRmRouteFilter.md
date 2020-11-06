---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 35f63b4655b92e42eb0a7d1bae70e2ef01c57a02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576901"
---
# <span data-ttu-id="d7a62-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d7a62-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="d7a62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7a62-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a62-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="d7a62-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7a62-104">SYNTAX</span></span>

### <span data-ttu-id="d7a62-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="d7a62-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7a62-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="d7a62-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7a62-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7a62-107">DESCRIPTION</span></span>
<span data-ttu-id="d7a62-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="d7a62-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d7a62-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7a62-109">EXAMPLES</span></span>

### <span data-ttu-id="d7a62-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d7a62-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d7a62-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="d7a62-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d7a62-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7a62-112">PARAMETERS</span></span>

### <span data-ttu-id="d7a62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a62-113">-DefaultProfile</span></span>
<span data-ttu-id="d7a62-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a62-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d7a62-115">-ExpandResource</span></span>
<span data-ttu-id="d7a62-116">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="d7a62-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a62-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7a62-117">-Name</span></span>
<span data-ttu-id="d7a62-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d7a62-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a62-119">-ResourceGroupName</span></span>
<span data-ttu-id="d7a62-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d7a62-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a62-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a62-121">CommonParameters</span></span>
<span data-ttu-id="d7a62-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a62-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a62-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a62-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a62-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7a62-124">INPUTS</span></span>

### <span data-ttu-id="d7a62-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a62-125">System.String</span></span>

## <span data-ttu-id="d7a62-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7a62-126">OUTPUTS</span></span>

### <span data-ttu-id="d7a62-127">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d7a62-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d7a62-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7a62-128">NOTES</span></span>

## <span data-ttu-id="d7a62-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7a62-129">RELATED LINKS</span></span>
