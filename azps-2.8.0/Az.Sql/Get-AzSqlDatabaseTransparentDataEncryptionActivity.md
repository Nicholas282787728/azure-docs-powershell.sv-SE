---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: bc072934fe8695cae0fd5f5762c1a31936997da9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920384"
---
# <span data-ttu-id="0a6b0-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="0a6b0-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="0a6b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6b0-103">Tar fram en TDE sökning av en databas.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="0a6b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a6b0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a6b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6b0-106">Cmdleten **Get-AzSqlDatabaseTransparentDataEncryptionActivity** får statusen för en TDE-genomsökning (transparent Data Encryption) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="0a6b0-107">Om ingen krypterings span körs returnerar denna cmdlet en tom lista.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="0a6b0-108">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="0a6b0-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0a6b0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a6b0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a6b0-111">Exempel 1: få TDE aktivitet för en databas</span><span class="sxs-lookup"><span data-stu-id="0a6b0-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="0a6b0-112">Det här kommandot hämtar TDE-aktiviteten för databasen som heter database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="0a6b0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a6b0-113">PARAMETERS</span></span>

### <span data-ttu-id="0a6b0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a6b0-114">-DatabaseName</span></span>
<span data-ttu-id="0a6b0-115">Anger namnet på den databas där cmdleten TDE krypterings aktivitet.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="0a6b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6b0-116">-DefaultProfile</span></span>
<span data-ttu-id="0a6b0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0a6b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a6b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="0a6b0-119">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0a6b0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a6b0-120">-ServerName</span></span>
<span data-ttu-id="0a6b0-121">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0a6b0-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a6b0-122">-Confirm</span></span>
<span data-ttu-id="0a6b0-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6b0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6b0-124">-WhatIf</span></span>
<span data-ttu-id="0a6b0-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6b0-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6b0-127">CommonParameters</span></span>
<span data-ttu-id="0a6b0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6b0-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a6b0-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6b0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a6b0-130">INPUTS</span></span>

### <span data-ttu-id="0a6b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0a6b0-131">System.String</span></span>

## <span data-ttu-id="0a6b0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a6b0-132">OUTPUTS</span></span>

### <span data-ttu-id="0a6b0-133">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="0a6b0-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="0a6b0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a6b0-134">NOTES</span></span>

## <span data-ttu-id="0a6b0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a6b0-135">RELATED LINKS</span></span>

[<span data-ttu-id="0a6b0-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0a6b0-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="0a6b0-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0a6b0-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


