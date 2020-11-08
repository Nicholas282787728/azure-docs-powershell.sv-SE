---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099493"
---
# <span data-ttu-id="73d34-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="73d34-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="73d34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73d34-102">SYNOPSIS</span></span>
<span data-ttu-id="73d34-103">Hämtar virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="73d34-103">Gets virtual networks.</span></span>

## <span data-ttu-id="73d34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73d34-104">SYNTAX</span></span>

### <span data-ttu-id="73d34-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="73d34-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73d34-106">FromId</span><span class="sxs-lookup"><span data-stu-id="73d34-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73d34-107">FromName</span><span class="sxs-lookup"><span data-stu-id="73d34-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73d34-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73d34-108">DESCRIPTION</span></span>
<span data-ttu-id="73d34-109">Cmdleten **Get-WAPackVNet** hämtar virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="73d34-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="73d34-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73d34-110">EXAMPLES</span></span>

### <span data-ttu-id="73d34-111">Exempel 1: Hämta alla virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="73d34-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="73d34-112">Det här kommandot får alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="73d34-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="73d34-113">Exempel 2: skaffa ett virtuellt nätverk genom att använda ett ID</span><span class="sxs-lookup"><span data-stu-id="73d34-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="73d34-114">Det här kommandot får det virtuella nätverk som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="73d34-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="73d34-115">Exempel 3: skaffa ett virtuellt nätverk genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="73d34-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="73d34-116">Det här kommandot får det virtuella nätverket som heter ContosoVNet08.</span><span class="sxs-lookup"><span data-stu-id="73d34-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="73d34-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73d34-117">PARAMETERS</span></span>

### <span data-ttu-id="73d34-118">-ID</span><span class="sxs-lookup"><span data-stu-id="73d34-118">-ID</span></span>
<span data-ttu-id="73d34-119">Anger det unika ID: t för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="73d34-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d34-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="73d34-120">-Name</span></span>
<span data-ttu-id="73d34-121">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="73d34-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d34-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="73d34-122">-Profile</span></span>
<span data-ttu-id="73d34-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="73d34-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73d34-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="73d34-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73d34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d34-125">CommonParameters</span></span>
<span data-ttu-id="73d34-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d34-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d34-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d34-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73d34-128">INPUTS</span></span>

## <span data-ttu-id="73d34-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73d34-129">OUTPUTS</span></span>

## <span data-ttu-id="73d34-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73d34-130">NOTES</span></span>

## <span data-ttu-id="73d34-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73d34-131">RELATED LINKS</span></span>

