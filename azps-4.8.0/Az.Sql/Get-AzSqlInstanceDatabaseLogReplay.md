---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260975"
---
# <span data-ttu-id="17816-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="17816-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="17816-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17816-102">SYNOPSIS</span></span>
<span data-ttu-id="17816-103">Hämtar statusen för loggning av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="17816-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="17816-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17816-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17816-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17816-105">DESCRIPTION</span></span>
<span data-ttu-id="17816-106">Cmdleten **Get-AzSqlInstanceDatabaseLogReplay** hämtar statusen för loggnings tjänsten för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="17816-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="17816-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17816-107">EXAMPLES</span></span>

### <span data-ttu-id="17816-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17816-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="17816-109">Det här kommandot får statusen för loggnings tjänsten för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="17816-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="17816-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17816-110">PARAMETERS</span></span>

### <span data-ttu-id="17816-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17816-111">-DefaultProfile</span></span>
<span data-ttu-id="17816-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17816-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17816-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="17816-113">-InstanceName</span></span>
<span data-ttu-id="17816-114">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="17816-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="17816-115">-Name</span></span>
<span data-ttu-id="17816-116">Namnet på instans databasen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="17816-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17816-117">-ResourceGroupName</span></span>
<span data-ttu-id="17816-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="17816-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="17816-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17816-119">CommonParameters</span></span>
<span data-ttu-id="17816-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17816-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17816-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17816-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17816-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17816-122">INPUTS</span></span>

### <span data-ttu-id="17816-123">System. String</span><span class="sxs-lookup"><span data-stu-id="17816-123">System.String</span></span>

## <span data-ttu-id="17816-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17816-124">OUTPUTS</span></span>

### <span data-ttu-id="17816-125">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="17816-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="17816-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17816-126">NOTES</span></span>

## <span data-ttu-id="17816-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17816-127">RELATED LINKS</span></span>
