---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757114"
---
# <span data-ttu-id="97aab-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="97aab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97aab-102">SYNOPSIS</span></span>
<span data-ttu-id="97aab-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="97aab-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97aab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97aab-104">SYNTAX</span></span>

### <span data-ttu-id="97aab-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="97aab-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97aab-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="97aab-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97aab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97aab-107">DESCRIPTION</span></span>
<span data-ttu-id="97aab-108">Cmdleten **Start-AzureRmVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="97aab-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="97aab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97aab-109">EXAMPLES</span></span>

### <span data-ttu-id="97aab-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="97aab-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="97aab-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="97aab-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="97aab-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97aab-112">PARAMETERS</span></span>

### <span data-ttu-id="97aab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97aab-113">-AsJob</span></span>
<span data-ttu-id="97aab-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="97aab-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="97aab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97aab-115">-DefaultProfile</span></span>
<span data-ttu-id="97aab-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97aab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97aab-117">-ID</span><span class="sxs-lookup"><span data-stu-id="97aab-117">-Id</span></span>
<span data-ttu-id="97aab-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="97aab-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97aab-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="97aab-119">-Name</span></span>
<span data-ttu-id="97aab-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="97aab-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="97aab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97aab-121">-ResourceGroupName</span></span>
<span data-ttu-id="97aab-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="97aab-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97aab-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97aab-123">-Confirm</span></span>
<span data-ttu-id="97aab-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97aab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97aab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97aab-125">-WhatIf</span></span>
<span data-ttu-id="97aab-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97aab-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97aab-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97aab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97aab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97aab-128">CommonParameters</span></span>
<span data-ttu-id="97aab-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97aab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97aab-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97aab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97aab-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97aab-131">INPUTS</span></span>

### <span data-ttu-id="97aab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="97aab-132">System.String</span></span>

## <span data-ttu-id="97aab-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97aab-133">OUTPUTS</span></span>

### <span data-ttu-id="97aab-134">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="97aab-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="97aab-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97aab-135">NOTES</span></span>

## <span data-ttu-id="97aab-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97aab-136">RELATED LINKS</span></span>

[<span data-ttu-id="97aab-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="97aab-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="97aab-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="97aab-140">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="97aab-141">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="97aab-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="97aab-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


