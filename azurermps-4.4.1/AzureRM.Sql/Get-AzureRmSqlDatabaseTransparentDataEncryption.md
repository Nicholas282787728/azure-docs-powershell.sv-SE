---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0566396e3a32891b010b2bfa3cd71ba47d4a7e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574975"
---
# <span data-ttu-id="4918d-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4918d-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="4918d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4918d-102">SYNOPSIS</span></span>
<span data-ttu-id="4918d-103">Hämtar TDE-tillståndet för en databas.</span><span class="sxs-lookup"><span data-stu-id="4918d-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4918d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4918d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4918d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4918d-105">DESCRIPTION</span></span>
<span data-ttu-id="4918d-106">Cmdleten **Get-AzureRmSqlDatabaseTransparentDataEncryption** får statusen för transparent Data Encryption (TDE) för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4918d-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="4918d-107">Mer information finns i transparent data kryptering med Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="4918d-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="4918d-108">Denna cmdlet hämtar det aktuella tillståndet för TDE, men både kryptering och dekryptering kan vara krävande.</span><span class="sxs-lookup"><span data-stu-id="4918d-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="4918d-109">Kör cmdleten Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity om du vill se hur krypterings genomsökningen fortskrider.</span><span class="sxs-lookup"><span data-stu-id="4918d-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="4918d-110">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="4918d-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4918d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4918d-111">EXAMPLES</span></span>

### <span data-ttu-id="4918d-112">Exempel 1: Hämta TDE status för en databas</span><span class="sxs-lookup"><span data-stu-id="4918d-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="4918d-113">Det här kommandot får statusen för TDE för databasen som heter Database01 på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="4918d-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="4918d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4918d-114">PARAMETERS</span></span>

### <span data-ttu-id="4918d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4918d-115">-DatabaseName</span></span>
<span data-ttu-id="4918d-116">Anger namnet på den databas där denna cmdlet ska TDE status.</span><span class="sxs-lookup"><span data-stu-id="4918d-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="4918d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4918d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4918d-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="4918d-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4918d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4918d-119">-ServerName</span></span>
<span data-ttu-id="4918d-120">Anger namnet på den server som är värd för databasen för vilken denna cmdlet får status TDE.</span><span class="sxs-lookup"><span data-stu-id="4918d-120">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="4918d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4918d-121">-Confirm</span></span>
<span data-ttu-id="4918d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4918d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4918d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4918d-123">-WhatIf</span></span>
<span data-ttu-id="4918d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4918d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4918d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4918d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4918d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4918d-126">-DefaultProfile</span></span>
<span data-ttu-id="4918d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4918d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4918d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4918d-128">CommonParameters</span></span>
<span data-ttu-id="4918d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4918d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4918d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4918d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4918d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4918d-131">INPUTS</span></span>

## <span data-ttu-id="4918d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4918d-132">OUTPUTS</span></span>

### <span data-ttu-id="4918d-133">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="4918d-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="4918d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4918d-134">NOTES</span></span>

## <span data-ttu-id="4918d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4918d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4918d-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="4918d-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="4918d-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4918d-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
