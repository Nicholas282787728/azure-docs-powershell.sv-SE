---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929462"
---
# <span data-ttu-id="06d9a-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="06d9a-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="06d9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="06d9a-103">Återkallar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="06d9a-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06d9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06d9a-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d9a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="06d9a-106">Cmdleten **REVOKE-AzureRmDiskAccess** avvisar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="06d9a-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="06d9a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="06d9a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06d9a-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="06d9a-109">Återkalla åtkomsten till disken "Disk01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="06d9a-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="06d9a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="06d9a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d9a-111">-AsJob</span></span>
<span data-ttu-id="06d9a-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06d9a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d9a-113">-DefaultProfile</span></span>
<span data-ttu-id="06d9a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06d9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d9a-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="06d9a-115">-DiskName</span></span>
<span data-ttu-id="06d9a-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="06d9a-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="06d9a-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="06d9a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d9a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06d9a-119">-Confirm</span></span>
<span data-ttu-id="06d9a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06d9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d9a-121">-WhatIf</span></span>
<span data-ttu-id="06d9a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06d9a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06d9a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06d9a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d9a-124">CommonParameters</span></span>
<span data-ttu-id="06d9a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d9a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d9a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d9a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06d9a-127">INPUTS</span></span>

### <span data-ttu-id="06d9a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="06d9a-128">System.String</span></span>

## <span data-ttu-id="06d9a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06d9a-129">OUTPUTS</span></span>

### <span data-ttu-id="06d9a-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="06d9a-130">System.Object</span></span>

## <span data-ttu-id="06d9a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06d9a-131">NOTES</span></span>

## <span data-ttu-id="06d9a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06d9a-132">RELATED LINKS</span></span>

