---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: f74abc2daab0c79c9d070d206a82b33fb15f23f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581912"
---
# <span data-ttu-id="fe1c6-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe1c6-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="fe1c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1c6-103">Anger att en databas använder gransknings principen för sin värd Server.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe1c6-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe1c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe1c6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1c6-106">Cmdleten **use-AzureRmSqlServerAuditingPolicy** anger att en databas använder gransknings principen för sin värd Server.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="fe1c6-107">Ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fe1c6-108">Om ingen gransknings princip har definierats för databas servern Miss lyckas denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="fe1c6-109">Om värden använder granskning på server nivå tas hot identifiering bort.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="fe1c6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe1c6-110">EXAMPLES</span></span>

### <span data-ttu-id="fe1c6-111">Exempel 1: Konfigurera en databas så att den använder gransknings principen för dess Server</span><span class="sxs-lookup"><span data-stu-id="fe1c6-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="fe1c6-112">Det här kommandot anger att databasen som heter Database01 på Server02 använder serverns gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="fe1c6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe1c6-113">PARAMETERS</span></span>

### <span data-ttu-id="fe1c6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe1c6-114">-DatabaseName</span></span>
<span data-ttu-id="fe1c6-115">Anger namnet på den databas som ska använda gransknings principen.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="fe1c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1c6-116">-DefaultProfile</span></span>
<span data-ttu-id="fe1c6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fe1c6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe1c6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe1c6-118">-PassThru</span></span>
<span data-ttu-id="fe1c6-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe1c6-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe1c6-122">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fe1c6-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe1c6-123">-ServerName</span></span>
<span data-ttu-id="fe1c6-124">Anger namnet på den server som är värd för databasen där gransknings principen används.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="fe1c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1c6-125">CommonParameters</span></span>
<span data-ttu-id="fe1c6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1c6-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1c6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe1c6-128">INPUTS</span></span>

### <span data-ttu-id="fe1c6-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="fe1c6-129">None</span></span>
<span data-ttu-id="fe1c6-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fe1c6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe1c6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe1c6-131">OUTPUTS</span></span>

### <span data-ttu-id="fe1c6-132">Microsoft. Azure. commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fe1c6-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="fe1c6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe1c6-133">NOTES</span></span>

## <span data-ttu-id="fe1c6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe1c6-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe1c6-135">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe1c6-135">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fe1c6-136">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe1c6-136">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="fe1c6-137">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe1c6-137">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="fe1c6-138">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="fe1c6-138">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="fe1c6-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fe1c6-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


