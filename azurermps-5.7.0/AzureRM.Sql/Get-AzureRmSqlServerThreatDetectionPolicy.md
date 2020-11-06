---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5ee1039f938c561424ded9768e9d5f84372410fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573171"
---
# <span data-ttu-id="aa3f2-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa3f2-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="aa3f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3f2-103">Hämtar principen för hot identifiering för en server.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa3f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa3f2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa3f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa3f2-105">DESCRIPTION</span></span>
<span data-ttu-id="aa3f2-106">Cmdleten **Get-AzureRmSqlServerThreatDetectionPolicy** hämtar hot Detection policyn för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="aa3f2-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* och *servername* för att identifiera den server som den här cmdleten får principen för.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="aa3f2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa3f2-108">EXAMPLES</span></span>

### <span data-ttu-id="aa3f2-109">Exempel 1: Hämta policyn för hot identifiering för en server</span><span class="sxs-lookup"><span data-stu-id="aa3f2-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="aa3f2-110">Det här kommandot får principen för hot identifiering för en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="aa3f2-111">Servern har tilldelats till resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="aa3f2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa3f2-112">PARAMETERS</span></span>

### <span data-ttu-id="aa3f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3f2-113">-DefaultProfile</span></span>
<span data-ttu-id="aa3f2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa3f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa3f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa3f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa3f2-116">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="aa3f2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa3f2-117">-ServerName</span></span>
<span data-ttu-id="aa3f2-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-118">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3f2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa3f2-119">-Confirm</span></span>
<span data-ttu-id="aa3f2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3f2-121">-WhatIf</span></span>
<span data-ttu-id="aa3f2-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3f2-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3f2-124">CommonParameters</span></span>
<span data-ttu-id="aa3f2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3f2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa3f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3f2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa3f2-127">INPUTS</span></span>

### <span data-ttu-id="aa3f2-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="aa3f2-128">None</span></span>
<span data-ttu-id="aa3f2-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="aa3f2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa3f2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa3f2-130">OUTPUTS</span></span>

### <span data-ttu-id="aa3f2-131">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="aa3f2-131">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="aa3f2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa3f2-132">NOTES</span></span>

## <span data-ttu-id="aa3f2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa3f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa3f2-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa3f2-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="aa3f2-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="aa3f2-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


