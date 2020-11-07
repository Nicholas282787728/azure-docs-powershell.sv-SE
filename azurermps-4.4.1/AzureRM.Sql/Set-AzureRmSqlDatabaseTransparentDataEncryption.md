---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755624"
---
# <span data-ttu-id="5ceea-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5ceea-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="5ceea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ceea-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceea-103">Ändrar egenskapen TDE för en databas.</span><span class="sxs-lookup"><span data-stu-id="5ceea-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ceea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ceea-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ceea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ceea-105">DESCRIPTION</span></span>
<span data-ttu-id="5ceea-106">Cmdleten **set-AzureRmSqlDatabaseTransparentDataEncryption** ändrar egenskapen transparent Data Encryption (TDE) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="5ceea-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="5ceea-107">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="5ceea-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="5ceea-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceea-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5ceea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ceea-109">EXAMPLES</span></span>

### <span data-ttu-id="5ceea-110">Exempel 1: Aktivera TDE för en databas</span><span class="sxs-lookup"><span data-stu-id="5ceea-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="5ceea-111">Det här kommandot aktiverar TDE för databasen som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="5ceea-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="5ceea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ceea-112">PARAMETERS</span></span>

### <span data-ttu-id="5ceea-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ceea-113">-DatabaseName</span></span>
<span data-ttu-id="5ceea-114">Anger namnet på den databas som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5ceea-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ceea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ceea-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ceea-116">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="5ceea-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5ceea-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ceea-117">-ServerName</span></span>
<span data-ttu-id="5ceea-118">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="5ceea-118">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5ceea-119">-State</span><span class="sxs-lookup"><span data-stu-id="5ceea-119">-State</span></span>
<span data-ttu-id="5ceea-120">Anger värdet för egenskapen TDE.</span><span class="sxs-lookup"><span data-stu-id="5ceea-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="5ceea-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5ceea-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ceea-122">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="5ceea-122">Enabled</span></span> 
- <span data-ttu-id="5ceea-123">Aktiv</span><span class="sxs-lookup"><span data-stu-id="5ceea-123">Disabled</span></span>

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

### <span data-ttu-id="5ceea-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ceea-124">-Confirm</span></span>
<span data-ttu-id="5ceea-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ceea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ceea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ceea-126">-WhatIf</span></span>
<span data-ttu-id="5ceea-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ceea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ceea-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ceea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ceea-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceea-129">-DefaultProfile</span></span>
<span data-ttu-id="5ceea-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceea-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ceea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceea-131">CommonParameters</span></span>
<span data-ttu-id="5ceea-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ceea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceea-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ceea-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceea-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ceea-134">INPUTS</span></span>

## <span data-ttu-id="5ceea-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ceea-135">OUTPUTS</span></span>

### <span data-ttu-id="5ceea-136">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="5ceea-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="5ceea-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ceea-137">NOTES</span></span>

## <span data-ttu-id="5ceea-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ceea-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ceea-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5ceea-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="5ceea-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="5ceea-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="5ceea-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5ceea-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


