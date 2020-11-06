---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574004"
---
# <span data-ttu-id="711e1-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="711e1-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="711e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="711e1-102">SYNOPSIS</span></span>
<span data-ttu-id="711e1-103">Tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="711e1-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="711e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="711e1-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="711e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="711e1-105">DESCRIPTION</span></span>
<span data-ttu-id="711e1-106">Cmdleten **Remove-AzureRmSnapshot** tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="711e1-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="711e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="711e1-107">EXAMPLES</span></span>

### <span data-ttu-id="711e1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="711e1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="711e1-109">Det här kommandot tar bort stillbilden "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="711e1-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="711e1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="711e1-110">PARAMETERS</span></span>

### <span data-ttu-id="711e1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="711e1-111">-AsJob</span></span>
<span data-ttu-id="711e1-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="711e1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711e1-113">-DefaultProfile</span></span>
<span data-ttu-id="711e1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="711e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="711e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="711e1-115">-Force</span></span>
<span data-ttu-id="711e1-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="711e1-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="711e1-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="711e1-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="711e1-119">-SnapshotName</span></span>
<span data-ttu-id="711e1-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="711e1-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="711e1-121">-Confirm</span></span>
<span data-ttu-id="711e1-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="711e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711e1-123">-WhatIf</span></span>
<span data-ttu-id="711e1-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="711e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711e1-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="711e1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711e1-126">CommonParameters</span></span>
<span data-ttu-id="711e1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="711e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711e1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="711e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711e1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="711e1-129">INPUTS</span></span>

### <span data-ttu-id="711e1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="711e1-130">System.String</span></span>

## <span data-ttu-id="711e1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="711e1-131">OUTPUTS</span></span>

### <span data-ttu-id="711e1-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="711e1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="711e1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="711e1-133">NOTES</span></span>

## <span data-ttu-id="711e1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="711e1-134">RELATED LINKS</span></span>
