---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387876"
---
# <span data-ttu-id="3288f-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="3288f-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="3288f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3288f-102">SYNOPSIS</span></span>
<span data-ttu-id="3288f-103">Tar bort ett Azure SQL-virtuellt kluster.</span><span class="sxs-lookup"><span data-stu-id="3288f-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="3288f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3288f-104">SYNTAX</span></span>

### <span data-ttu-id="3288f-105">RemoveVirtualClusterFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="3288f-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3288f-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="3288f-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3288f-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="3288f-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3288f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3288f-108">DESCRIPTION</span></span>
<span data-ttu-id="3288f-109">Cmdleten **Remove-AzSqlVirtualCluster** tar bort ett virtuellt Azure SQL-kluster.</span><span class="sxs-lookup"><span data-stu-id="3288f-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="3288f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3288f-110">EXAMPLES</span></span>

### <span data-ttu-id="3288f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3288f-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="3288f-112">Det här kommandot tar bort det virtuella klustret med namnet VirtualCluster1 tilldelat resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3288f-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3288f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3288f-113">PARAMETERS</span></span>

### <span data-ttu-id="3288f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3288f-114">-AsJob</span></span>
<span data-ttu-id="3288f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3288f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3288f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3288f-116">-DefaultProfile</span></span>
<span data-ttu-id="3288f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3288f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3288f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3288f-118">-InputObject</span></span>
<span data-ttu-id="3288f-119">Instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="3288f-119">The instance object to remove</span></span>

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

### <span data-ttu-id="3288f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3288f-120">-Name</span></span>
<span data-ttu-id="3288f-121">Namnet på det virtuella klustret.</span><span class="sxs-lookup"><span data-stu-id="3288f-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="3288f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3288f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3288f-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3288f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3288f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3288f-124">-ResourceId</span></span>
<span data-ttu-id="3288f-125">Resurs-ID för instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="3288f-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="3288f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3288f-126">-Confirm</span></span>
<span data-ttu-id="3288f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3288f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3288f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3288f-128">-WhatIf</span></span>
<span data-ttu-id="3288f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3288f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3288f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3288f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3288f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3288f-131">CommonParameters</span></span>
<span data-ttu-id="3288f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3288f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3288f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3288f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3288f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3288f-134">INPUTS</span></span>

### <span data-ttu-id="3288f-135">Microsoft. Azure. commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="3288f-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="3288f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3288f-136">System.String</span></span>

## <span data-ttu-id="3288f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3288f-137">OUTPUTS</span></span>

### <span data-ttu-id="3288f-138">Microsoft. Azure. commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="3288f-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="3288f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3288f-139">NOTES</span></span>

## <span data-ttu-id="3288f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3288f-140">RELATED LINKS</span></span>
