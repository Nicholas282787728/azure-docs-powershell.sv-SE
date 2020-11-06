---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 843a3bd4cd3d43239cfb850edc3cd3b4fb3461ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586168"
---
# <span data-ttu-id="b02f7-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b02f7-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b02f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b02f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b02f7-103">Avbryter datareplikeringen mellan en SQL-databas och den angivna sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="b02f7-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b02f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b02f7-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b02f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b02f7-106">Cmdleten **Remove-AzureRmSqlDatabaseSecondary** tvingar fram en geo-replikeringslänk.</span><span class="sxs-lookup"><span data-stu-id="b02f7-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="b02f7-107">Denna cmdlet ersätter Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02f7-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="b02f7-108">Det finns ingen replikerings-synkronisering före uppsägning.</span><span class="sxs-lookup"><span data-stu-id="b02f7-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="b02f7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b02f7-109">EXAMPLES</span></span>

## <span data-ttu-id="b02f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b02f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b02f7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b02f7-111">-DatabaseName</span></span>
<span data-ttu-id="b02f7-112">Anger namnet på den primära Azure SQL-databas som innehåller replikeringslänken som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="b02f7-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b02f7-113">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02f7-113">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b02f7-114">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b02f7-114">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="b02f7-115">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b02f7-115">-PartnerServerName</span></span>
<span data-ttu-id="b02f7-116">Anger namnet på partner-SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="b02f7-116">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="b02f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b02f7-118">Anger namnet på den resurs grupp som är kopplad till replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b02f7-118">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="b02f7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b02f7-119">-ServerName</span></span>
<span data-ttu-id="b02f7-120">Anger namnet på den SQL Server som innehåller replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b02f7-120">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="b02f7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b02f7-121">-Confirm</span></span>
<span data-ttu-id="b02f7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b02f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02f7-123">-WhatIf</span></span>
<span data-ttu-id="b02f7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b02f7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02f7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b02f7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02f7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02f7-126">-DefaultProfile</span></span>
<span data-ttu-id="b02f7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b02f7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02f7-128">CommonParameters</span></span>
<span data-ttu-id="b02f7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02f7-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02f7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b02f7-131">INPUTS</span></span>

###  
<span data-ttu-id="b02f7-132">Du kan pipe-instanser för **den primära** eller sekundära databasen till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02f7-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="b02f7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b02f7-133">OUTPUTS</span></span>

###  
<span data-ttu-id="b02f7-134">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b02f7-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b02f7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b02f7-135">NOTES</span></span>

## <span data-ttu-id="b02f7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b02f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="b02f7-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b02f7-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b02f7-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b02f7-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b02f7-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b02f7-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
