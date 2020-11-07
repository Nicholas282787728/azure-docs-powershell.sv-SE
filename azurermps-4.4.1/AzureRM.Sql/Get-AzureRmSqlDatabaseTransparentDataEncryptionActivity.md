---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755499"
---
# <span data-ttu-id="de3f3-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="de3f3-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="de3f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="de3f3-103">Tar fram en TDE sökning av en databas.</span><span class="sxs-lookup"><span data-stu-id="de3f3-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de3f3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de3f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="de3f3-106">Cmdleten **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** får statusen för en TDE-genomsökning (transparent Data Encryption) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="de3f3-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="de3f3-107">Om ingen krypterings span körs returnerar denna cmdlet en tom lista.</span><span class="sxs-lookup"><span data-stu-id="de3f3-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="de3f3-108">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="de3f3-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="de3f3-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="de3f3-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="de3f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de3f3-110">EXAMPLES</span></span>

### <span data-ttu-id="de3f3-111">Exempel 1: få TDE aktivitet för en databas</span><span class="sxs-lookup"><span data-stu-id="de3f3-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="de3f3-112">Det här kommandot hämtar TDE-aktiviteten för databasen som heter database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="de3f3-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="de3f3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de3f3-113">PARAMETERS</span></span>

### <span data-ttu-id="de3f3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de3f3-114">-DatabaseName</span></span>
<span data-ttu-id="de3f3-115">Anger namnet på den databas där cmdleten TDE krypterings aktivitet.</span><span class="sxs-lookup"><span data-stu-id="de3f3-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="de3f3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3f3-116">-ResourceGroupName</span></span>
<span data-ttu-id="de3f3-117">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="de3f3-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="de3f3-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de3f3-118">-ServerName</span></span>
<span data-ttu-id="de3f3-119">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="de3f3-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="de3f3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de3f3-120">-Confirm</span></span>
<span data-ttu-id="de3f3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de3f3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3f3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3f3-122">-WhatIf</span></span>
<span data-ttu-id="de3f3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de3f3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de3f3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de3f3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3f3-125">-DefaultProfile</span></span>
<span data-ttu-id="de3f3-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de3f3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3f3-127">CommonParameters</span></span>
<span data-ttu-id="de3f3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3f3-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3f3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de3f3-130">INPUTS</span></span>

## <span data-ttu-id="de3f3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de3f3-131">OUTPUTS</span></span>

### <span data-ttu-id="de3f3-132">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="de3f3-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="de3f3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de3f3-133">NOTES</span></span>

## <span data-ttu-id="de3f3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de3f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="de3f3-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="de3f3-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="de3f3-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="de3f3-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


