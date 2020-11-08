---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100121"
---
# <span data-ttu-id="a60ac-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="a60ac-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="a60ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a60ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a60ac-103">Returnerar statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="a60ac-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="a60ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a60ac-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a60ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a60ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a60ac-106">Returnerar statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="a60ac-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="a60ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a60ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a60ac-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="a60ac-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="a60ac-109">Få statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="a60ac-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="a60ac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a60ac-110">PARAMETERS</span></span>

### <span data-ttu-id="a60ac-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a60ac-111">-FarmName</span></span>
<span data-ttu-id="a60ac-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="a60ac-112">Farm Id.</span></span>

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

### <span data-ttu-id="a60ac-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="a60ac-113">-JobId</span></span>
<span data-ttu-id="a60ac-114">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="a60ac-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60ac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60ac-115">-ResourceGroupName</span></span>
<span data-ttu-id="a60ac-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a60ac-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60ac-117">CommonParameters</span></span>
<span data-ttu-id="a60ac-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60ac-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60ac-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60ac-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a60ac-120">INPUTS</span></span>

## <span data-ttu-id="a60ac-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a60ac-121">OUTPUTS</span></span>

### <span data-ttu-id="a60ac-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="a60ac-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="a60ac-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a60ac-123">NOTES</span></span>

## <span data-ttu-id="a60ac-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a60ac-124">RELATED LINKS</span></span>
