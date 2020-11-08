---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926981"
---
# <span data-ttu-id="b8afe-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="b8afe-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="b8afe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8afe-102">SYNOPSIS</span></span>
<span data-ttu-id="b8afe-103">Tar bort en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b8afe-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="b8afe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8afe-104">SYNTAX</span></span>

### <span data-ttu-id="b8afe-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="b8afe-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8afe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b8afe-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8afe-107">ID</span><span class="sxs-lookup"><span data-stu-id="b8afe-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8afe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8afe-108">DESCRIPTION</span></span>
<span data-ttu-id="b8afe-109">Remove-AzSqlVM cmdlet tar bort en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b8afe-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="b8afe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8afe-110">EXAMPLES</span></span>

### <span data-ttu-id="b8afe-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8afe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="b8afe-112">Tar bort den virtuella Azure SQL-datorn "VM" i resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b8afe-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b8afe-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8afe-113">PARAMETERS</span></span>

### <span data-ttu-id="b8afe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8afe-114">-AsJob</span></span>
<span data-ttu-id="b8afe-115">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="b8afe-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b8afe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8afe-116">-DefaultProfile</span></span>
<span data-ttu-id="b8afe-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8afe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8afe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8afe-118">-InputObject</span></span>
<span data-ttu-id="b8afe-119">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="b8afe-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8afe-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8afe-120">-Name</span></span>
<span data-ttu-id="b8afe-121">Namn på SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b8afe-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8afe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8afe-122">-PassThru</span></span>
<span data-ttu-id="b8afe-123">Anger om den borttagna resursen ska matas ut i slutet av cmdlet-körningen.</span><span class="sxs-lookup"><span data-stu-id="b8afe-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="b8afe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8afe-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8afe-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b8afe-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8afe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8afe-126">-ResourceId</span></span>
<span data-ttu-id="b8afe-127">Resurs-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="b8afe-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8afe-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8afe-128">-Confirm</span></span>
<span data-ttu-id="b8afe-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8afe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8afe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8afe-130">-WhatIf</span></span>
<span data-ttu-id="b8afe-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8afe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8afe-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8afe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8afe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8afe-133">CommonParameters</span></span>
<span data-ttu-id="b8afe-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8afe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8afe-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8afe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8afe-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8afe-136">INPUTS</span></span>

### <span data-ttu-id="b8afe-137">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b8afe-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b8afe-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8afe-138">OUTPUTS</span></span>

### <span data-ttu-id="b8afe-139">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b8afe-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b8afe-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8afe-140">NOTES</span></span>

## <span data-ttu-id="b8afe-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8afe-141">RELATED LINKS</span></span>