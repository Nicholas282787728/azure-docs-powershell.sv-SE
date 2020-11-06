---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: ec7c452939d82b82deed507c667bdc9cdeab3cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579340"
---
# <span data-ttu-id="899f4-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="899f4-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="899f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="899f4-102">SYNOPSIS</span></span>
<span data-ttu-id="899f4-103">Tar fram en TDE sökning av en databas.</span><span class="sxs-lookup"><span data-stu-id="899f4-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="899f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="899f4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="899f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="899f4-105">DESCRIPTION</span></span>
<span data-ttu-id="899f4-106">Cmdleten **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** får statusen för en TDE-genomsökning (transparent Data Encryption) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="899f4-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="899f4-107">Om ingen krypterings span körs returnerar denna cmdlet en tom lista.</span><span class="sxs-lookup"><span data-stu-id="899f4-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="899f4-108">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="899f4-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="899f4-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="899f4-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="899f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="899f4-110">EXAMPLES</span></span>

### <span data-ttu-id="899f4-111">Exempel 1: få TDE aktivitet för en databas</span><span class="sxs-lookup"><span data-stu-id="899f4-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="899f4-112">Det här kommandot hämtar TDE-aktiviteten för databasen som heter database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="899f4-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="899f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="899f4-113">PARAMETERS</span></span>

### <span data-ttu-id="899f4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="899f4-114">-DatabaseName</span></span>
<span data-ttu-id="899f4-115">Anger namnet på den databas där cmdleten TDE krypterings aktivitet.</span><span class="sxs-lookup"><span data-stu-id="899f4-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899f4-116">-DefaultProfile</span></span>
<span data-ttu-id="899f4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="899f4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="899f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="899f4-119">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="899f4-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="899f4-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="899f4-120">-ServerName</span></span>
<span data-ttu-id="899f4-121">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="899f4-121">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899f4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="899f4-122">-Confirm</span></span>
<span data-ttu-id="899f4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="899f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899f4-124">-WhatIf</span></span>
<span data-ttu-id="899f4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="899f4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899f4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="899f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="899f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899f4-127">CommonParameters</span></span>
<span data-ttu-id="899f4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899f4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899f4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="899f4-130">INPUTS</span></span>

### <span data-ttu-id="899f4-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="899f4-131">None</span></span>
<span data-ttu-id="899f4-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="899f4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="899f4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="899f4-133">OUTPUTS</span></span>

### <span data-ttu-id="899f4-134">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="899f4-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="899f4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="899f4-135">NOTES</span></span>

## <span data-ttu-id="899f4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="899f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="899f4-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="899f4-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="899f4-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="899f4-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


