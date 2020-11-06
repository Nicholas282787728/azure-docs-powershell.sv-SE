---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: bd61b666dd321ec9007d413030cb899eeeb92778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583744"
---
# <span data-ttu-id="7dc61-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="7dc61-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="7dc61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dc61-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc61-103">Startar uppgraderingen av en SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="7dc61-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dc61-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dc61-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc61-106">Cmdleten **Start-AzureRmSqlServerUpgrade** startar uppgraderingen av en Azure SQL Database Server version 11 till version 12.</span><span class="sxs-lookup"><span data-stu-id="7dc61-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="7dc61-107">Du kan övervaka förloppet för en uppgradering med hjälp av Get-AzureRmSqlServerUpgrade cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dc61-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="7dc61-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dc61-108">EXAMPLES</span></span>

### <span data-ttu-id="7dc61-109">Exempel 1: uppgradera en server</span><span class="sxs-lookup"><span data-stu-id="7dc61-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="7dc61-110">Det här kommandot uppgraderar den server som heter Server01 tilldelad till resurs gruppen TesourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7dc61-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="7dc61-111">Exempel 2: uppgradera en server med hjälp av schema tid och databas rekommendation</span><span class="sxs-lookup"><span data-stu-id="7dc61-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="7dc61-112">Det första kommandot skapar en tid om fem minuter i framtiden med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dc61-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="7dc61-113">Kommandot lagrar datumet i variabeln $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="7dc61-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="7dc61-114">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7dc61-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="7dc61-115">Det andra kommandot skapar ett **RecommendedDatabaseProperties** -objekt och lagrar sedan objektet i variabeln $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="7dc61-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>

<span data-ttu-id="7dc61-116">Nästa tre kommandon tilldelar värden till egenskaper för det objekt som lagras i $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="7dc61-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>

<span data-ttu-id="7dc61-117">Det sista kommandot uppgraderar den befintliga servern som heter Server01 till version 12,0.</span><span class="sxs-lookup"><span data-stu-id="7dc61-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="7dc61-118">Den tidigaste tiden för uppgraderingen är fem minuter efter att du har kört kommandot enligt $ScheduleTime variabel.</span><span class="sxs-lookup"><span data-stu-id="7dc61-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="7dc61-119">Efter uppgraderingen kör databas ContosoDB standard versionen och har tjänst nivå mål S0.</span><span class="sxs-lookup"><span data-stu-id="7dc61-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="7dc61-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dc61-120">PARAMETERS</span></span>

### <span data-ttu-id="7dc61-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="7dc61-121">-DatabaseCollection</span></span>
<span data-ttu-id="7dc61-122">Anger en matris med **RecommendedDatabaseProperties** -objekt som denna cmdlet använder för Server uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="7dc61-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc61-123">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="7dc61-123">-ElasticPoolCollection</span></span>
<span data-ttu-id="7dc61-124">Anger en matris med **UpgradeRecommendedElasticPoolProperties** -objekt som ska användas för Server uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="7dc61-124">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc61-125">-ResourceGroupName</span></span>
<span data-ttu-id="7dc61-126">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7dc61-126">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7dc61-127">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="7dc61-127">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="7dc61-128">Anger den tidigaste tiden, som ett **datetime** -objekt, för att uppgradera servern.</span><span class="sxs-lookup"><span data-stu-id="7dc61-128">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="7dc61-129">Ange ett värde i ISO8601-format i UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="7dc61-129">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="7dc61-130">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7dc61-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc61-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7dc61-131">-ServerName</span></span>
<span data-ttu-id="7dc61-132">Anger namnet på den server som cmdleten uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="7dc61-132">Specifies the name of the server that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="7dc61-133">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="7dc61-133">-ServerVersion</span></span>
<span data-ttu-id="7dc61-134">Anger den version som denna cmdlet uppgraderar till servern.</span><span class="sxs-lookup"><span data-stu-id="7dc61-134">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="7dc61-135">Det enda giltiga värdet är 12,0.</span><span class="sxs-lookup"><span data-stu-id="7dc61-135">The only valid value is 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc61-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc61-136">-DefaultProfile</span></span>
<span data-ttu-id="7dc61-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc61-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc61-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc61-138">CommonParameters</span></span>
<span data-ttu-id="7dc61-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc61-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc61-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc61-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc61-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dc61-141">INPUTS</span></span>

## <span data-ttu-id="7dc61-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dc61-142">OUTPUTS</span></span>

### <span data-ttu-id="7dc61-143">Microsoft. Azure. commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="7dc61-143">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="7dc61-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dc61-144">NOTES</span></span>

## <span data-ttu-id="7dc61-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dc61-145">RELATED LINKS</span></span>

[<span data-ttu-id="7dc61-146">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="7dc61-146">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="7dc61-147">Stopp-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="7dc61-147">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="7dc61-148">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7dc61-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


