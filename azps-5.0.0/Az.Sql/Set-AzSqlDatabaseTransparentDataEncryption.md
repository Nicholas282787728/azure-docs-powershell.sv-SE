---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270193"
---
# <span data-ttu-id="1913c-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1913c-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="1913c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1913c-102">SYNOPSIS</span></span>
<span data-ttu-id="1913c-103">Ändrar egenskapen TDE för en databas.</span><span class="sxs-lookup"><span data-stu-id="1913c-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="1913c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1913c-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1913c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1913c-105">DESCRIPTION</span></span>
<span data-ttu-id="1913c-106">Cmdleten **set-AzSqlDatabaseTransparentDataEncryption** ändrar egenskapen transparent Data Encryption (TDE) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1913c-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="1913c-107">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="1913c-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="1913c-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="1913c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1913c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1913c-109">EXAMPLES</span></span>

### <span data-ttu-id="1913c-110">Exempel 1: Aktivera TDE för en databas</span><span class="sxs-lookup"><span data-stu-id="1913c-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="1913c-111">Det här kommandot aktiverar TDE för databasen som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="1913c-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="1913c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1913c-112">PARAMETERS</span></span>

### <span data-ttu-id="1913c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1913c-113">-DatabaseName</span></span>
<span data-ttu-id="1913c-114">Anger namnet på den databas som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="1913c-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1913c-115">-DefaultProfile</span></span>
<span data-ttu-id="1913c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1913c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1913c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1913c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1913c-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="1913c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1913c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1913c-119">-ServerName</span></span>
<span data-ttu-id="1913c-120">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="1913c-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1913c-121">-State</span><span class="sxs-lookup"><span data-stu-id="1913c-121">-State</span></span>
<span data-ttu-id="1913c-122">Anger värdet för egenskapen TDE.</span><span class="sxs-lookup"><span data-stu-id="1913c-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="1913c-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1913c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1913c-124">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="1913c-124">Enabled</span></span> 
- <span data-ttu-id="1913c-125">Aktiv</span><span class="sxs-lookup"><span data-stu-id="1913c-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913c-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1913c-126">-Confirm</span></span>
<span data-ttu-id="1913c-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1913c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1913c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1913c-128">-WhatIf</span></span>
<span data-ttu-id="1913c-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1913c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1913c-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1913c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1913c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1913c-131">CommonParameters</span></span>
<span data-ttu-id="1913c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1913c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1913c-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1913c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1913c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1913c-134">INPUTS</span></span>

### <span data-ttu-id="1913c-135">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="1913c-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="1913c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1913c-136">System.String</span></span>

## <span data-ttu-id="1913c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1913c-137">OUTPUTS</span></span>

### <span data-ttu-id="1913c-138">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="1913c-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="1913c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1913c-139">NOTES</span></span>

## <span data-ttu-id="1913c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1913c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1913c-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1913c-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="1913c-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="1913c-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="1913c-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1913c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

