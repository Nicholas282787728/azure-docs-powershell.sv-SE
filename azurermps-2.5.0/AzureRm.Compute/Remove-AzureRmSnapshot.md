---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930646"
---
# <span data-ttu-id="5a824-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5a824-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="5a824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a824-102">SYNOPSIS</span></span>
<span data-ttu-id="5a824-103">Tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="5a824-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a824-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a824-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a824-105">DESCRIPTION</span></span>
<span data-ttu-id="5a824-106">Cmdleten **Remove-AzureRmSnapshot** tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="5a824-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="5a824-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a824-107">EXAMPLES</span></span>

### <span data-ttu-id="5a824-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a824-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="5a824-109">Det här kommandot tar bort stillbilden "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5a824-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5a824-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a824-110">PARAMETERS</span></span>

### <span data-ttu-id="5a824-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a824-111">-AsJob</span></span>
<span data-ttu-id="5a824-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="5a824-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5a824-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a824-113">-DefaultProfile</span></span>
<span data-ttu-id="5a824-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a824-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a824-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5a824-115">-Force</span></span>
<span data-ttu-id="5a824-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5a824-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a824-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a824-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a824-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5a824-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5a824-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5a824-119">-SnapshotName</span></span>
<span data-ttu-id="5a824-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="5a824-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5a824-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a824-121">-Confirm</span></span>
<span data-ttu-id="5a824-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a824-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a824-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a824-123">-WhatIf</span></span>
<span data-ttu-id="5a824-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a824-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a824-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a824-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a824-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a824-126">CommonParameters</span></span>
<span data-ttu-id="5a824-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a824-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a824-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a824-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a824-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a824-129">INPUTS</span></span>

### <span data-ttu-id="5a824-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5a824-130">System.String</span></span>

## <span data-ttu-id="5a824-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a824-131">OUTPUTS</span></span>

### <span data-ttu-id="5a824-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="5a824-132">System.Object</span></span>

## <span data-ttu-id="5a824-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a824-133">NOTES</span></span>

## <span data-ttu-id="5a824-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a824-134">RELATED LINKS</span></span>

