---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262914"
---
# <span data-ttu-id="90e0d-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="90e0d-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="90e0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="90e0d-103">Tar bort gransknings inställningar för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="90e0d-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="90e0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90e0d-104">SYNTAX</span></span>

### <span data-ttu-id="90e0d-105">ServerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="90e0d-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e0d-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90e0d-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e0d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="90e0d-108">Cmdleten **Remove-AzSqlServerAudit** tar bort gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90e0d-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="90e0d-109">Ange parametrarna *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="90e0d-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="90e0d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="90e0d-111">Exempel 1: ta bort gransknings inställningarna för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="90e0d-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="90e0d-112">Exempel 2: ta bort, genom pipeline, gransknings inställningarna för en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="90e0d-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="90e0d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90e0d-113">PARAMETERS</span></span>

### <span data-ttu-id="90e0d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90e0d-114">-AsJob</span></span>
<span data-ttu-id="90e0d-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="90e0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90e0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e0d-116">-DefaultProfile</span></span>
<span data-ttu-id="90e0d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90e0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="90e0d-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="90e0d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="90e0d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90e0d-120">-ServerName</span></span>
<span data-ttu-id="90e0d-121">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="90e0d-121">SQL server name.</span></span>

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

### <span data-ttu-id="90e0d-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="90e0d-122">-ServerObject</span></span>
<span data-ttu-id="90e0d-123">Serverobjektet för att hantera dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="90e0d-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="90e0d-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90e0d-124">-Confirm</span></span>
<span data-ttu-id="90e0d-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90e0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e0d-126">-WhatIf</span></span>
<span data-ttu-id="90e0d-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90e0d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90e0d-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90e0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e0d-129">CommonParameters</span></span>
<span data-ttu-id="90e0d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e0d-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90e0d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e0d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90e0d-132">INPUTS</span></span>

### <span data-ttu-id="90e0d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="90e0d-133">System.String</span></span>

### <span data-ttu-id="90e0d-134">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="90e0d-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="90e0d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90e0d-135">OUTPUTS</span></span>

### <span data-ttu-id="90e0d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90e0d-136">System.Boolean</span></span>

## <span data-ttu-id="90e0d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90e0d-137">NOTES</span></span>

## <span data-ttu-id="90e0d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90e0d-138">RELATED LINKS</span></span>