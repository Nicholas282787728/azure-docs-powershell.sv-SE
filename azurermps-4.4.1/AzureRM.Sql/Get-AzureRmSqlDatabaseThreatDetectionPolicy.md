---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ed1e01b5d49aaf31404f1db4d55fd31a253faca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574976"
---
# <span data-ttu-id="addf4-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="addf4-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="addf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="addf4-102">SYNOPSIS</span></span>
<span data-ttu-id="addf4-103">Hämtar principen för hot identifiering för en databas.</span><span class="sxs-lookup"><span data-stu-id="addf4-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="addf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="addf4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="addf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="addf4-105">DESCRIPTION</span></span>
<span data-ttu-id="addf4-106">Cmdleten **Get-AzureRmSqlDatabaseThreatDetectionPolicy** hämtar hot Detection policyn för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="addf4-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="addf4-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera den databas som den här cmdleten får principen för.</span><span class="sxs-lookup"><span data-stu-id="addf4-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="addf4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="addf4-108">EXAMPLES</span></span>

### <span data-ttu-id="addf4-109">Exempel 1: Hämta policyn för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="addf4-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="addf4-110">Det här kommandot får principen för hot identifiering för en databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="addf4-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="addf4-111">Databasen finns på den server som heter Server01, vilken är tilldelad till resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="addf4-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="addf4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="addf4-112">PARAMETERS</span></span>

### <span data-ttu-id="addf4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="addf4-113">-DatabaseName</span></span>
<span data-ttu-id="addf4-114">Anger namnet på en databas.</span><span class="sxs-lookup"><span data-stu-id="addf4-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="addf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="addf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="addf4-116">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="addf4-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="addf4-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="addf4-117">-ServerName</span></span>
<span data-ttu-id="addf4-118">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="addf4-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="addf4-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="addf4-119">-Confirm</span></span>
<span data-ttu-id="addf4-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="addf4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="addf4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="addf4-121">-WhatIf</span></span>
<span data-ttu-id="addf4-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="addf4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="addf4-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="addf4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="addf4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addf4-124">-DefaultProfile</span></span>
<span data-ttu-id="addf4-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="addf4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="addf4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addf4-126">CommonParameters</span></span>
<span data-ttu-id="addf4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addf4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addf4-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addf4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addf4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="addf4-129">INPUTS</span></span>

###  
<span data-ttu-id="addf4-130">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="addf4-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="addf4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="addf4-131">OUTPUTS</span></span>

### <span data-ttu-id="addf4-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="addf4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="addf4-133">Denna cmdlet returnerar ett **Model. DatabaseThreatDetectionPolicyModel** -objekt.</span><span class="sxs-lookup"><span data-stu-id="addf4-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="addf4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="addf4-134">NOTES</span></span>

## <span data-ttu-id="addf4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="addf4-135">RELATED LINKS</span></span>

[<span data-ttu-id="addf4-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="addf4-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



