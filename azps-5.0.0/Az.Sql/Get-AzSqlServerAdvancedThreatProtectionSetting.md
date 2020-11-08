---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272665"
---
# <span data-ttu-id="a7eb0-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a7eb0-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a7eb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="a7eb0-103">Hämtar inställningar för avancerat skydd för en server.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="a7eb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7eb0-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7eb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="a7eb0-106">Cmdleten **Get-AzSqlServerAdvancedThreatProtectionSetting** får avancerade skydds inställningar för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="a7eb0-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* och *servername* för att identifiera den server som den här cmdleten får inställningar för.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="a7eb0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7eb0-108">EXAMPLES</span></span>

### <span data-ttu-id="a7eb0-109">Exempel 1: Hämta avancerade skydds inställningar för en server</span><span class="sxs-lookup"><span data-stu-id="a7eb0-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="a7eb0-110">Det här kommandot får avancerade inställningar för skydd mot en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="a7eb0-111">Servern har tilldelats till resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a7eb0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7eb0-112">PARAMETERS</span></span>

### <span data-ttu-id="a7eb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7eb0-113">-DefaultProfile</span></span>
<span data-ttu-id="a7eb0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a7eb0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7eb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7eb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7eb0-116">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="a7eb0-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7eb0-117">-ServerName</span></span>
<span data-ttu-id="a7eb0-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a7eb0-119">-Confirm</span></span>
<span data-ttu-id="a7eb0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7eb0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7eb0-121">-WhatIf</span></span>
<span data-ttu-id="a7eb0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7eb0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7eb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7eb0-124">CommonParameters</span></span>
<span data-ttu-id="a7eb0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7eb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7eb0-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7eb0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7eb0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7eb0-127">INPUTS</span></span>

### <span data-ttu-id="a7eb0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a7eb0-128">System.String</span></span>

## <span data-ttu-id="a7eb0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7eb0-129">OUTPUTS</span></span>

### <span data-ttu-id="a7eb0-130">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a7eb0-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="a7eb0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7eb0-131">NOTES</span></span>

## <span data-ttu-id="a7eb0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7eb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7eb0-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a7eb0-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="a7eb0-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a7eb0-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


