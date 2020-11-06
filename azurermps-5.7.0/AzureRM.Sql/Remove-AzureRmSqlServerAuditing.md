---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bd5d8d2c63b10ecc4aaabd5e96ab1ce844602325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576398"
---
# <span data-ttu-id="a24c0-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a24c0-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="a24c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a24c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a24c0-103">Tar bort granskningen av en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="a24c0-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a24c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a24c0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a24c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a24c0-106">Cmdleten **Remove-AzureRmSqlServerAuditing** tar bort granskningen av en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="a24c0-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="a24c0-107">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="a24c0-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="a24c0-108">När du har kört denna cmdlet utförs inte granskning av databaserna på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a24c0-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="a24c0-109">Om kommandot lyckas och du anger parametern *Passthru* returnerar cmdleten ett objekt som beskriver den aktuella gransknings principen och Azure SQL Server-identifierarna.</span><span class="sxs-lookup"><span data-stu-id="a24c0-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="a24c0-110">Server-ID: n innehåller **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="a24c0-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="a24c0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a24c0-111">EXAMPLES</span></span>

### <span data-ttu-id="a24c0-112">Exempel 1: ta bort granskningen av en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="a24c0-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a24c0-113">Det här kommandot tar bort granskningen av alla databaser som finns på Server01 i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a24c0-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="a24c0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a24c0-114">PARAMETERS</span></span>

### <span data-ttu-id="a24c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24c0-115">-DefaultProfile</span></span>
<span data-ttu-id="a24c0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a24c0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a24c0-117">-PassThru</span></span>
<span data-ttu-id="a24c0-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a24c0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a24c0-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a24c0-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24c0-120">-ResourceGroupName</span></span>
<span data-ttu-id="a24c0-121">Anger namnet på den resurs grupp som Azure SQL-servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="a24c0-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a24c0-122">-ServerName</span></span>
<span data-ttu-id="a24c0-123">Anger namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="a24c0-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a24c0-124">-Confirm</span></span>
<span data-ttu-id="a24c0-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a24c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24c0-126">-WhatIf</span></span>
<span data-ttu-id="a24c0-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a24c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a24c0-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a24c0-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24c0-129">CommonParameters</span></span>
<span data-ttu-id="a24c0-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24c0-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24c0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24c0-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a24c0-132">INPUTS</span></span>

### <span data-ttu-id="a24c0-133">Microsoft. Azure. commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a24c0-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="a24c0-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a24c0-134">OUTPUTS</span></span>

### <span data-ttu-id="a24c0-135">Microsoft. Azure. commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a24c0-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="a24c0-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a24c0-136">NOTES</span></span>

## <span data-ttu-id="a24c0-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a24c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="a24c0-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a24c0-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="a24c0-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a24c0-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="a24c0-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a24c0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


