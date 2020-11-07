---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931266"
---
# <span data-ttu-id="27eab-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27eab-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="27eab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27eab-102">SYNOPSIS</span></span>
<span data-ttu-id="27eab-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="27eab-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27eab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27eab-104">SYNTAX</span></span>

### <span data-ttu-id="27eab-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="27eab-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27eab-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="27eab-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27eab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27eab-107">DESCRIPTION</span></span>
<span data-ttu-id="27eab-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="27eab-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="27eab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27eab-109">EXAMPLES</span></span>

### <span data-ttu-id="27eab-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27eab-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="27eab-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="27eab-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="27eab-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27eab-112">PARAMETERS</span></span>

### <span data-ttu-id="27eab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27eab-113">-DefaultProfile</span></span>
<span data-ttu-id="27eab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27eab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27eab-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="27eab-115">-ExpandResource</span></span>
<span data-ttu-id="27eab-116">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="27eab-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="27eab-117">-Name</span></span>
<span data-ttu-id="27eab-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="27eab-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27eab-119">-ResourceGroupName</span></span>
<span data-ttu-id="27eab-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="27eab-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27eab-121">CommonParameters</span></span>
<span data-ttu-id="27eab-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27eab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27eab-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27eab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27eab-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27eab-124">INPUTS</span></span>

### <span data-ttu-id="27eab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27eab-125">System.String</span></span>

## <span data-ttu-id="27eab-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27eab-126">OUTPUTS</span></span>

### <span data-ttu-id="27eab-127">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="27eab-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="27eab-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27eab-128">NOTES</span></span>

## <span data-ttu-id="27eab-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27eab-129">RELATED LINKS</span></span>

