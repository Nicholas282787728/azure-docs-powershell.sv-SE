---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419635"
---
# <span data-ttu-id="f926a-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f926a-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f926a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f926a-102">SYNOPSIS</span></span>
<span data-ttu-id="f926a-103">Tar bort de avancerade skydds inställningarna från en databas.</span><span class="sxs-lookup"><span data-stu-id="f926a-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="f926a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f926a-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f926a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f926a-105">DESCRIPTION</span></span>
<span data-ttu-id="f926a-106">Cmdleten **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** tar bort avancerade skydds inställningar från en AzureAzure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f926a-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="f926a-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* och *servername* för att identifiera den databas som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f926a-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="f926a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f926a-108">EXAMPLES</span></span>

### <span data-ttu-id="f926a-109">Exempel 1: ta bort avancerade skydds inställningar för en databas</span><span class="sxs-lookup"><span data-stu-id="f926a-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f926a-110">Det här kommandot tar bort de avancerade skydds inställningarna från en databas som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="f926a-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="f926a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f926a-111">PARAMETERS</span></span>

### <span data-ttu-id="f926a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f926a-112">-DatabaseName</span></span>
<span data-ttu-id="f926a-113">Anger namnet på en databas där inställningarna för avancerat skydd ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f926a-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="f926a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f926a-114">-DefaultProfile</span></span>
<span data-ttu-id="f926a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f926a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f926a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f926a-116">-PassThru</span></span>
<span data-ttu-id="f926a-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f926a-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f926a-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f926a-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f926a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f926a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f926a-120">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="f926a-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="f926a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f926a-121">-ServerName</span></span>
<span data-ttu-id="f926a-122">Anger namnet på en server som databasen körs på.</span><span class="sxs-lookup"><span data-stu-id="f926a-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="f926a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f926a-123">-Confirm</span></span>
<span data-ttu-id="f926a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f926a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f926a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f926a-125">-WhatIf</span></span>
<span data-ttu-id="f926a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f926a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f926a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f926a-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f926a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f926a-128">CommonParameters</span></span>
<span data-ttu-id="f926a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f926a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f926a-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f926a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f926a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f926a-131">INPUTS</span></span>

### <span data-ttu-id="f926a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f926a-132">System.String</span></span>

## <span data-ttu-id="f926a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f926a-133">OUTPUTS</span></span>

### <span data-ttu-id="f926a-134">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="f926a-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="f926a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f926a-135">NOTES</span></span>

## <span data-ttu-id="f926a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f926a-136">RELATED LINKS</span></span>

[<span data-ttu-id="f926a-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f926a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


