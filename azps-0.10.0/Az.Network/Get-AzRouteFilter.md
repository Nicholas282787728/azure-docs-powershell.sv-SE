---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922223"
---
# <span data-ttu-id="a02f3-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a02f3-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="a02f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a02f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a02f3-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="a02f3-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="a02f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a02f3-104">SYNTAX</span></span>

### <span data-ttu-id="a02f3-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="a02f3-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a02f3-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="a02f3-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a02f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a02f3-107">DESCRIPTION</span></span>
<span data-ttu-id="a02f3-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="a02f3-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a02f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a02f3-109">EXAMPLES</span></span>

### <span data-ttu-id="a02f3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a02f3-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a02f3-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="a02f3-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="a02f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a02f3-112">PARAMETERS</span></span>

### <span data-ttu-id="a02f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02f3-113">-DefaultProfile</span></span>
<span data-ttu-id="a02f3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a02f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a02f3-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a02f3-115">-ExpandResource</span></span>
<span data-ttu-id="a02f3-116">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="a02f3-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="a02f3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a02f3-117">-Name</span></span>
<span data-ttu-id="a02f3-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a02f3-118">The resource name.</span></span>

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

### <span data-ttu-id="a02f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a02f3-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a02f3-120">The resource group name.</span></span>

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

### <span data-ttu-id="a02f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02f3-121">CommonParameters</span></span>
<span data-ttu-id="a02f3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02f3-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02f3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02f3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a02f3-124">INPUTS</span></span>

### <span data-ttu-id="a02f3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a02f3-125">System.String</span></span>

## <span data-ttu-id="a02f3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a02f3-126">OUTPUTS</span></span>

### <span data-ttu-id="a02f3-127">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a02f3-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a02f3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a02f3-128">NOTES</span></span>

## <span data-ttu-id="a02f3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a02f3-129">RELATED LINKS</span></span>

