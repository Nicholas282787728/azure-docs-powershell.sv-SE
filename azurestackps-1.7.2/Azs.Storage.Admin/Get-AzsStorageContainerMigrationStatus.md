---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921152"
---
# <span data-ttu-id="2bfc0-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="2bfc0-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="2bfc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfc0-103">Returnerar statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="2bfc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bfc0-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bfc0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bfc0-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfc0-106">Returnerar statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="2bfc0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bfc0-107">EXAMPLES</span></span>

### <span data-ttu-id="2bfc0-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2bfc0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="2bfc0-109">Få statusen för ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="2bfc0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bfc0-110">PARAMETERS</span></span>

### <span data-ttu-id="2bfc0-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="2bfc0-111">-FarmName</span></span>
<span data-ttu-id="2bfc0-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-112">Farm Id.</span></span>

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

### <span data-ttu-id="2bfc0-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="2bfc0-113">-JobId</span></span>
<span data-ttu-id="2bfc0-114">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-114">Operation Id.</span></span>

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

### <span data-ttu-id="2bfc0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfc0-115">-ResourceGroupName</span></span>
<span data-ttu-id="2bfc0-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-116">Resource group name.</span></span>

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

### <span data-ttu-id="2bfc0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfc0-117">CommonParameters</span></span>
<span data-ttu-id="2bfc0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfc0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfc0-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfc0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfc0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bfc0-120">INPUTS</span></span>

## <span data-ttu-id="2bfc0-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bfc0-121">OUTPUTS</span></span>

### <span data-ttu-id="2bfc0-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="2bfc0-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="2bfc0-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bfc0-123">NOTES</span></span>

## <span data-ttu-id="2bfc0-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bfc0-124">RELATED LINKS</span></span>

