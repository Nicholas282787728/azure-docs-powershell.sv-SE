---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520511"
---
# <span data-ttu-id="0d0d8-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="0d0d8-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="0d0d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0d8-103">Tar bort ett Azure SQL-virtuellt kluster.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="0d0d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d0d8-104">SYNTAX</span></span>

### <span data-ttu-id="0d0d8-105">RemoveVirtualClusterFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="0d0d8-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0d8-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="0d0d8-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0d8-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0d8-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d0d8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d0d8-108">DESCRIPTION</span></span>
<span data-ttu-id="0d0d8-109">Cmdleten **Remove-AzSqlVirtualCluster** tar bort ett virtuellt Azure SQL-kluster.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="0d0d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d0d8-110">EXAMPLES</span></span>

### <span data-ttu-id="0d0d8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d0d8-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="0d0d8-112">Det här kommandot tar bort det virtuella klustret med namnet VirtualCluster1 tilldelat resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0d0d8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d0d8-113">PARAMETERS</span></span>

### <span data-ttu-id="0d0d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d0d8-114">-AsJob</span></span>
<span data-ttu-id="0d0d8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0d0d8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d0d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0d8-116">-DefaultProfile</span></span>
<span data-ttu-id="0d0d8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d0d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d0d8-118">-InputObject</span></span>
<span data-ttu-id="0d0d8-119">Instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="0d0d8-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0d8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d0d8-120">-Name</span></span>
<span data-ttu-id="0d0d8-121">Namnet på det virtuella klustret.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d0d8-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0d8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0d8-124">-ResourceId</span></span>
<span data-ttu-id="0d0d8-125">Resurs-ID för instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="0d0d8-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0d8-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d0d8-126">-Confirm</span></span>
<span data-ttu-id="0d0d8-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d0d8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0d8-128">-WhatIf</span></span>
<span data-ttu-id="0d0d8-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d0d8-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d0d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0d8-131">CommonParameters</span></span>
<span data-ttu-id="0d0d8-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d0d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0d8-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d0d8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0d8-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d0d8-134">INPUTS</span></span>

### <span data-ttu-id="0d0d8-135">Microsoft. Azure. commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="0d0d8-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="0d0d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0d0d8-136">System.String</span></span>

## <span data-ttu-id="0d0d8-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d0d8-137">OUTPUTS</span></span>

### <span data-ttu-id="0d0d8-138">Microsoft. Azure. commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="0d0d8-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="0d0d8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d0d8-139">NOTES</span></span>

## <span data-ttu-id="0d0d8-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d0d8-140">RELATED LINKS</span></span>
