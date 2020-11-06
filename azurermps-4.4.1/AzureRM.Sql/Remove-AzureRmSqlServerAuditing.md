---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: ed77001a8eb2a6c0a7869f5aefbbaa93017ede22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574479"
---
# <span data-ttu-id="d7d73-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="d7d73-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="d7d73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7d73-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d73-103">Tar bort granskningen av en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="d7d73-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7d73-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d73-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7d73-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d73-106">Cmdleten **Remove-AzureRmSqlServerAuditing** tar bort granskningen av en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="d7d73-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="d7d73-107">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="d7d73-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="d7d73-108">När du har kört denna cmdlet utförs inte granskning av databaserna på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7d73-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="d7d73-109">Om kommandot lyckas och du anger parametern *Passthru* returnerar cmdleten ett objekt som beskriver den aktuella gransknings principen och Azure SQL Server-identifierarna.</span><span class="sxs-lookup"><span data-stu-id="d7d73-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="d7d73-110">Server-ID: n innehåller **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="d7d73-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="d7d73-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7d73-111">EXAMPLES</span></span>

### <span data-ttu-id="d7d73-112">Exempel 1: ta bort granskningen av en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="d7d73-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="d7d73-113">Det här kommandot tar bort granskningen av alla databaser som finns på Server01 i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7d73-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="d7d73-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7d73-114">PARAMETERS</span></span>

### <span data-ttu-id="d7d73-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7d73-115">-PassThru</span></span>
<span data-ttu-id="d7d73-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d7d73-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7d73-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d7d73-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7d73-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d73-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7d73-119">Anger namnet på den resurs grupp som Azure SQL-servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="d7d73-119">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="d7d73-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7d73-120">-ServerName</span></span>
<span data-ttu-id="d7d73-121">Anger namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="d7d73-121">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d73-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7d73-122">-Confirm</span></span>
<span data-ttu-id="d7d73-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7d73-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d73-124">-WhatIf</span></span>
<span data-ttu-id="d7d73-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7d73-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d73-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7d73-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d73-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d73-127">-DefaultProfile</span></span>
<span data-ttu-id="d7d73-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d73-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d73-129">CommonParameters</span></span>
<span data-ttu-id="d7d73-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d73-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d73-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7d73-132">INPUTS</span></span>

### <span data-ttu-id="d7d73-133">Microsoft. Azure. commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d7d73-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="d7d73-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7d73-134">OUTPUTS</span></span>

### <span data-ttu-id="d7d73-135">Microsoft. Azure. commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d7d73-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="d7d73-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7d73-136">NOTES</span></span>

## <span data-ttu-id="d7d73-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7d73-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7d73-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7d73-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d7d73-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7d73-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d7d73-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d7d73-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


