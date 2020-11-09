---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325091"
---
# <span data-ttu-id="70017-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="70017-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="70017-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70017-102">SYNOPSIS</span></span>
<span data-ttu-id="70017-103">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="70017-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="70017-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70017-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="70017-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70017-105">DESCRIPTION</span></span>
<span data-ttu-id="70017-106">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="70017-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="70017-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70017-107">EXAMPLES</span></span>

### <span data-ttu-id="70017-108">Exempel 1: Hämta PostgreSql Server replik efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="70017-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="70017-109">Denna cmdlet får PostgreSql Server replik efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="70017-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="70017-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70017-110">PARAMETERS</span></span>

### <span data-ttu-id="70017-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70017-111">-DefaultProfile</span></span>
<span data-ttu-id="70017-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70017-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70017-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70017-113">-ResourceGroupName</span></span>
<span data-ttu-id="70017-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70017-114">The name of the resource group.</span></span>
<span data-ttu-id="70017-115">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="70017-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="70017-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70017-116">-ServerName</span></span>
<span data-ttu-id="70017-117">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="70017-117">The name of the server.</span></span>

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

### <span data-ttu-id="70017-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70017-118">-SubscriptionId</span></span>
<span data-ttu-id="70017-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="70017-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70017-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70017-120">CommonParameters</span></span>
<span data-ttu-id="70017-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70017-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70017-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70017-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70017-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70017-123">INPUTS</span></span>

## <span data-ttu-id="70017-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70017-124">OUTPUTS</span></span>

### <span data-ttu-id="70017-125">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="70017-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="70017-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70017-126">NOTES</span></span>

<span data-ttu-id="70017-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="70017-127">ALIASES</span></span>

## <span data-ttu-id="70017-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70017-128">RELATED LINKS</span></span>

