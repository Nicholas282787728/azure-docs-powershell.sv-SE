---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926977"
---
# <span data-ttu-id="925d0-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="925d0-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="925d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="925d0-102">SYNOPSIS</span></span>
<span data-ttu-id="925d0-103">Tar bort en virtuell SQL-gruppgrupp.</span><span class="sxs-lookup"><span data-stu-id="925d0-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="925d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="925d0-104">SYNTAX</span></span>

### <span data-ttu-id="925d0-105">ParamaterList (standard)</span><span class="sxs-lookup"><span data-stu-id="925d0-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="925d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="925d0-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="925d0-107">ID</span><span class="sxs-lookup"><span data-stu-id="925d0-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="925d0-108">Namn</span><span class="sxs-lookup"><span data-stu-id="925d0-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="925d0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="925d0-109">DESCRIPTION</span></span>
<span data-ttu-id="925d0-110">Remove-AzSqlVMGroup cmdlet tar bort en virtuell SQL-dator grupp.</span><span class="sxs-lookup"><span data-stu-id="925d0-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="925d0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="925d0-111">EXAMPLES</span></span>

### <span data-ttu-id="925d0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="925d0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="925d0-113">Tar bort gruppen "test grupp" i ResourceGroup01 för Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="925d0-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="925d0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="925d0-114">PARAMETERS</span></span>

### <span data-ttu-id="925d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="925d0-115">-AsJob</span></span>
<span data-ttu-id="925d0-116">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="925d0-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="925d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925d0-117">-DefaultProfile</span></span>
<span data-ttu-id="925d0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="925d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="925d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="925d0-119">-InputObject</span></span>
<span data-ttu-id="925d0-120">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="925d0-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="925d0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="925d0-121">-Name</span></span>
<span data-ttu-id="925d0-122">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="925d0-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="925d0-123">-PassThru</span></span>
<span data-ttu-id="925d0-124">Anger om den borttagna resursen ska matas ut i slutet av cmdlet-körningen.</span><span class="sxs-lookup"><span data-stu-id="925d0-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="925d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="925d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="925d0-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="925d0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="925d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="925d0-127">-ResourceId</span></span>
<span data-ttu-id="925d0-128">Grupp-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="925d0-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="925d0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="925d0-129">-Confirm</span></span>
<span data-ttu-id="925d0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="925d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="925d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="925d0-131">-WhatIf</span></span>
<span data-ttu-id="925d0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="925d0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="925d0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="925d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="925d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925d0-134">CommonParameters</span></span>
<span data-ttu-id="925d0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="925d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925d0-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="925d0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925d0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="925d0-137">INPUTS</span></span>

### <span data-ttu-id="925d0-138">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="925d0-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="925d0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="925d0-139">System.String</span></span>

## <span data-ttu-id="925d0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="925d0-140">OUTPUTS</span></span>

### <span data-ttu-id="925d0-141">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="925d0-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="925d0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="925d0-142">NOTES</span></span>

## <span data-ttu-id="925d0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="925d0-143">RELATED LINKS</span></span>
