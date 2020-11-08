---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272135"
---
# <span data-ttu-id="8771f-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="8771f-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="8771f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8771f-102">SYNOPSIS</span></span>
<span data-ttu-id="8771f-103">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="8771f-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="8771f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8771f-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8771f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8771f-105">DESCRIPTION</span></span>
<span data-ttu-id="8771f-106">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="8771f-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="8771f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8771f-107">EXAMPLES</span></span>

### <span data-ttu-id="8771f-108">Exempel 1: lista alla replik databaser under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="8771f-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8771f-109">Det här kommandot listar alla replik databaser under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8771f-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="8771f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8771f-110">PARAMETERS</span></span>

### <span data-ttu-id="8771f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8771f-111">-DefaultProfile</span></span>
<span data-ttu-id="8771f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8771f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8771f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8771f-113">-ResourceGroupName</span></span>
<span data-ttu-id="8771f-114">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="8771f-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8771f-115">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="8771f-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8771f-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8771f-116">-ServerName</span></span>
<span data-ttu-id="8771f-117">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="8771f-117">The name of the server.</span></span>

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

### <span data-ttu-id="8771f-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8771f-118">-SubscriptionId</span></span>
<span data-ttu-id="8771f-119">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8771f-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8771f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8771f-120">CommonParameters</span></span>
<span data-ttu-id="8771f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8771f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8771f-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8771f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8771f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8771f-123">INPUTS</span></span>

## <span data-ttu-id="8771f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8771f-124">OUTPUTS</span></span>

### <span data-ttu-id="8771f-125">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="8771f-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8771f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8771f-126">NOTES</span></span>

<span data-ttu-id="8771f-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8771f-127">ALIASES</span></span>

## <span data-ttu-id="8771f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8771f-128">RELATED LINKS</span></span>

