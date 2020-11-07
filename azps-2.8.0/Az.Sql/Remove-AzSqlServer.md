---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 52e0d37777b349744cf82f891fe8f711758f5a64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920268"
---
# <span data-ttu-id="e102f-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e102f-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="e102f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e102f-102">SYNOPSIS</span></span>
<span data-ttu-id="e102f-103">Tar bort en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="e102f-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="e102f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e102f-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e102f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e102f-105">DESCRIPTION</span></span>
<span data-ttu-id="e102f-106">Cmdleten **Remove-AzSqlServer** tar bort en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="e102f-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="e102f-107">Borttagnings åtgärden är asynkron och kan ta lite tid, så kontrol lera att åtgärden är klar innan du utför ytterligare åtgärder som beror på att servern tas bort helt.</span><span class="sxs-lookup"><span data-stu-id="e102f-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="e102f-108">Till exempel måste du skapa en ny server med samma namn.</span><span class="sxs-lookup"><span data-stu-id="e102f-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="e102f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e102f-109">EXAMPLES</span></span>

### <span data-ttu-id="e102f-110">Exempel 1: ta bort en server</span><span class="sxs-lookup"><span data-stu-id="e102f-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e102f-111">Det här kommandot tar bort Azure SQL-databasfilen med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="e102f-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="e102f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e102f-112">PARAMETERS</span></span>

### <span data-ttu-id="e102f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e102f-113">-DefaultProfile</span></span>
<span data-ttu-id="e102f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e102f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e102f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e102f-115">-Force</span></span>
<span data-ttu-id="e102f-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e102f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e102f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e102f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e102f-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="e102f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e102f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e102f-119">-ServerName</span></span>
<span data-ttu-id="e102f-120">Anger namnet på den server som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e102f-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e102f-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e102f-121">-Confirm</span></span>
<span data-ttu-id="e102f-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e102f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e102f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e102f-123">-WhatIf</span></span>
<span data-ttu-id="e102f-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e102f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e102f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e102f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e102f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e102f-126">CommonParameters</span></span>
<span data-ttu-id="e102f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e102f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e102f-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e102f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e102f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e102f-129">INPUTS</span></span>

### <span data-ttu-id="e102f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e102f-130">System.String</span></span>

## <span data-ttu-id="e102f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e102f-131">OUTPUTS</span></span>

### <span data-ttu-id="e102f-132">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e102f-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e102f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e102f-133">NOTES</span></span>

## <span data-ttu-id="e102f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e102f-134">RELATED LINKS</span></span>

[<span data-ttu-id="e102f-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e102f-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="e102f-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e102f-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e102f-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e102f-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="e102f-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e102f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


