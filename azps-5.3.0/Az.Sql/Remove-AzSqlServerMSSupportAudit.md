---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520527"
---
# <span data-ttu-id="18916-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="18916-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="18916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18916-102">SYNOPSIS</span></span>
<span data-ttu-id="18916-103">Tar bort Microsofts support åtgärder gransknings inställningar för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="18916-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="18916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18916-104">SYNTAX</span></span>

### <span data-ttu-id="18916-105">ServerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="18916-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18916-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18916-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18916-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18916-107">DESCRIPTION</span></span>
<span data-ttu-id="18916-108">Cmdleten **Remove-AzSqlServerMSSupportAudit** tar bort Microsofts support åtgärder gransknings inställningar för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="18916-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="18916-109">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="18916-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="18916-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18916-110">EXAMPLES</span></span>

### <span data-ttu-id="18916-111">Exempel 1: ta bort gransknings inställningar för Microsoft Support för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="18916-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="18916-112">Exempel 2: ta bort, genom pipeline, Microsofts support gransknings inställningar för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="18916-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="18916-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18916-113">PARAMETERS</span></span>

### <span data-ttu-id="18916-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18916-114">-AsJob</span></span>
<span data-ttu-id="18916-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18916-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18916-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18916-116">-DefaultProfile</span></span>
<span data-ttu-id="18916-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18916-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18916-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18916-118">-ResourceGroupName</span></span>
<span data-ttu-id="18916-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="18916-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18916-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18916-120">-ServerName</span></span>
<span data-ttu-id="18916-121">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="18916-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18916-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="18916-122">-ServerObject</span></span>
<span data-ttu-id="18916-123">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="18916-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18916-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18916-124">-Confirm</span></span>
<span data-ttu-id="18916-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18916-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18916-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18916-126">-WhatIf</span></span>
<span data-ttu-id="18916-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18916-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18916-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18916-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18916-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18916-129">CommonParameters</span></span>
<span data-ttu-id="18916-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18916-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18916-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18916-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18916-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18916-132">INPUTS</span></span>

### <span data-ttu-id="18916-133">System. String</span><span class="sxs-lookup"><span data-stu-id="18916-133">System.String</span></span>

### <span data-ttu-id="18916-134">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="18916-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="18916-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18916-135">OUTPUTS</span></span>

### <span data-ttu-id="18916-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18916-136">System.Boolean</span></span>

## <span data-ttu-id="18916-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18916-137">NOTES</span></span>

## <span data-ttu-id="18916-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18916-138">RELATED LINKS</span></span>
