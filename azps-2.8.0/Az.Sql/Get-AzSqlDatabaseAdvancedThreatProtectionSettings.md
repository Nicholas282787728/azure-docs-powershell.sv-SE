---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920425"
---
# <span data-ttu-id="ca42f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="ca42f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="ca42f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca42f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca42f-103">Hämtar avancerade skydds inställningar för en databas.</span><span class="sxs-lookup"><span data-stu-id="ca42f-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="ca42f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca42f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca42f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca42f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca42f-106">Cmdleten **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** får avancerade skydds inställningar för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ca42f-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="ca42f-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera den databas som den här cmdleten får inställningar för.</span><span class="sxs-lookup"><span data-stu-id="ca42f-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="ca42f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca42f-108">EXAMPLES</span></span>

### <span data-ttu-id="ca42f-109">Exempel 1: Hämta avancerade skydds inställningar för en databas</span><span class="sxs-lookup"><span data-stu-id="ca42f-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="ca42f-110">Det här kommandot får avancerade inställningar för skydd mot en databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="ca42f-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="ca42f-111">Databasen finns på den server som heter Server01, vilken är tilldelad till resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca42f-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ca42f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca42f-112">PARAMETERS</span></span>

### <span data-ttu-id="ca42f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca42f-113">-DatabaseName</span></span>
<span data-ttu-id="ca42f-114">Anger namnet på en databas.</span><span class="sxs-lookup"><span data-stu-id="ca42f-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="ca42f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca42f-115">-DefaultProfile</span></span>
<span data-ttu-id="ca42f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ca42f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca42f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca42f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca42f-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="ca42f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ca42f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca42f-119">-ServerName</span></span>
<span data-ttu-id="ca42f-120">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="ca42f-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="ca42f-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca42f-121">-Confirm</span></span>
<span data-ttu-id="ca42f-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca42f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca42f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca42f-123">-WhatIf</span></span>
<span data-ttu-id="ca42f-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca42f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca42f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca42f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca42f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca42f-126">CommonParameters</span></span>
<span data-ttu-id="ca42f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca42f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca42f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca42f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca42f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca42f-129">INPUTS</span></span>

### <span data-ttu-id="ca42f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ca42f-130">System.String</span></span>

## <span data-ttu-id="ca42f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca42f-131">OUTPUTS</span></span>

### <span data-ttu-id="ca42f-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ca42f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="ca42f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca42f-133">NOTES</span></span>

## <span data-ttu-id="ca42f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca42f-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca42f-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="ca42f-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)



