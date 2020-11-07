---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf6664023fbd43601c9b7c41a4f578809a9717c5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921892"
---
# <span data-ttu-id="df4c0-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="df4c0-101">Get-AzsTableService</span></span>

## <span data-ttu-id="df4c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="df4c0-103">Returnerar tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="df4c0-103">Returns the table service.</span></span>

## <span data-ttu-id="df4c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df4c0-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="df4c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="df4c0-106">Returnerar tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="df4c0-106">Returns the table service.</span></span>

## <span data-ttu-id="df4c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df4c0-107">EXAMPLES</span></span>

### <span data-ttu-id="df4c0-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="df4c0-108">EXAMPLE 1</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="df4c0-109">Skaffa tabellen service.</span><span class="sxs-lookup"><span data-stu-id="df4c0-109">Get the table servie.</span></span>

## <span data-ttu-id="df4c0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df4c0-110">PARAMETERS</span></span>

### <span data-ttu-id="df4c0-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="df4c0-111">-FarmName</span></span>
<span data-ttu-id="df4c0-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="df4c0-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4c0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4c0-113">-ResourceGroupName</span></span>
<span data-ttu-id="df4c0-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="df4c0-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4c0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4c0-115">CommonParameters</span></span>
<span data-ttu-id="df4c0-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4c0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4c0-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4c0-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4c0-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df4c0-118">INPUTS</span></span>

## <span data-ttu-id="df4c0-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df4c0-119">OUTPUTS</span></span>

### <span data-ttu-id="df4c0-120">Microsoft. AzureStack. Management. Storage. admin. Models. TableService</span><span class="sxs-lookup"><span data-stu-id="df4c0-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="df4c0-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df4c0-121">NOTES</span></span>

## <span data-ttu-id="df4c0-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df4c0-122">RELATED LINKS</span></span>
