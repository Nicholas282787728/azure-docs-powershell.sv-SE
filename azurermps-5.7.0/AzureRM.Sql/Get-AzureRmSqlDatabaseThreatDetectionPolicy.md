---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579351"
---
# <span data-ttu-id="e0dd8-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0dd8-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e0dd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dd8-103">Hämtar principen för hot identifiering för en databas.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0dd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0dd8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dd8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dd8-106">Cmdleten **Get-AzureRmSqlDatabaseThreatDetectionPolicy** hämtar hot Detection policyn för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="e0dd8-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera den databas som den här cmdleten får principen för.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="e0dd8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0dd8-108">EXAMPLES</span></span>

### <span data-ttu-id="e0dd8-109">Exempel 1: Hämta policyn för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="e0dd8-109">Example 1: Get the threat detection policy for a database</span></span>
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

<span data-ttu-id="e0dd8-110">Det här kommandot får principen för hot identifiering för en databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="e0dd8-111">Databasen finns på den server som heter Server01, vilken är tilldelad till resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e0dd8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0dd8-112">PARAMETERS</span></span>

### <span data-ttu-id="e0dd8-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0dd8-113">-DatabaseName</span></span>
<span data-ttu-id="e0dd8-114">Anger namnet på en databas.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="e0dd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dd8-115">-DefaultProfile</span></span>
<span data-ttu-id="e0dd8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0dd8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0dd8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dd8-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0dd8-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e0dd8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0dd8-119">-ServerName</span></span>
<span data-ttu-id="e0dd8-120">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="e0dd8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0dd8-121">-Confirm</span></span>
<span data-ttu-id="e0dd8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0dd8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dd8-123">-WhatIf</span></span>
<span data-ttu-id="e0dd8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0dd8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0dd8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dd8-126">CommonParameters</span></span>
<span data-ttu-id="e0dd8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dd8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dd8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dd8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0dd8-129">INPUTS</span></span>

###  
<span data-ttu-id="e0dd8-130">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e0dd8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0dd8-131">OUTPUTS</span></span>

### <span data-ttu-id="e0dd8-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e0dd8-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e0dd8-133">Denna cmdlet returnerar ett **Model. DatabaseThreatDetectionPolicyModel** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e0dd8-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e0dd8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0dd8-134">NOTES</span></span>

## <span data-ttu-id="e0dd8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0dd8-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0dd8-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0dd8-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



