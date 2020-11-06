---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 9b51a9e835962ea1715a458ace1ab02202068e30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579903"
---
# <span data-ttu-id="aa41d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa41d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="aa41d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa41d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa41d-103">Tar bort hot identifierings policyn från en databas.</span><span class="sxs-lookup"><span data-stu-id="aa41d-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa41d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa41d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa41d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa41d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa41d-106">Cmdleten **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** tar bort hot Detection policyn från en AzureAzure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="aa41d-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="aa41d-107">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* och *servername* för att identifiera den databas som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="aa41d-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="aa41d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa41d-108">EXAMPLES</span></span>

### <span data-ttu-id="aa41d-109">Exempel 1: ta bort en princip för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="aa41d-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="aa41d-110">Det här kommandot tar bort principen för hot identifiering från en databas som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="aa41d-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="aa41d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa41d-111">PARAMETERS</span></span>

### <span data-ttu-id="aa41d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa41d-112">-DatabaseName</span></span>
<span data-ttu-id="aa41d-113">Anger namnet på en databas där principen för hot identifiering ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aa41d-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="aa41d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa41d-114">-DefaultProfile</span></span>
<span data-ttu-id="aa41d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa41d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa41d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa41d-116">-PassThru</span></span>
<span data-ttu-id="aa41d-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="aa41d-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa41d-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="aa41d-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa41d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa41d-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa41d-120">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="aa41d-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="aa41d-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa41d-121">-ServerName</span></span>
<span data-ttu-id="aa41d-122">Anger namnet på en server som databasen körs på.</span><span class="sxs-lookup"><span data-stu-id="aa41d-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="aa41d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa41d-123">-Confirm</span></span>
<span data-ttu-id="aa41d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa41d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa41d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa41d-125">-WhatIf</span></span>
<span data-ttu-id="aa41d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa41d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa41d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa41d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa41d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa41d-128">CommonParameters</span></span>
<span data-ttu-id="aa41d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa41d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa41d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa41d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa41d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa41d-131">INPUTS</span></span>

### <span data-ttu-id="aa41d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="aa41d-132">System.String</span></span>

## <span data-ttu-id="aa41d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa41d-133">OUTPUTS</span></span>

### <span data-ttu-id="aa41d-134">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="aa41d-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="aa41d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa41d-135">NOTES</span></span>

## <span data-ttu-id="aa41d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa41d-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa41d-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="aa41d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


