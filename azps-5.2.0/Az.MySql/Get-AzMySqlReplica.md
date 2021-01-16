---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410168"
---
# <span data-ttu-id="7bc4b-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="7bc4b-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="7bc4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc4b-103">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="7bc4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bc4b-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7bc4b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bc4b-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc4b-106">Lista alla replikerna för en given server.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="7bc4b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bc4b-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc4b-108">Exempel 1: skaffa Server replik för MySql efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="7bc4b-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="7bc4b-109">Denna cmdlet får MySql-Server replik efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="7bc4b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bc4b-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc4b-111">-DefaultProfile</span></span>
<span data-ttu-id="7bc4b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc4b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc4b-113">-ResourceGroupName</span></span>
<span data-ttu-id="7bc4b-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-114">The name of the resource group.</span></span>
<span data-ttu-id="7bc4b-115">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7bc4b-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7bc4b-116">-ServerName</span></span>
<span data-ttu-id="7bc4b-117">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-117">The name of the server.</span></span>

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

### <span data-ttu-id="7bc4b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc4b-118">-SubscriptionId</span></span>
<span data-ttu-id="7bc4b-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7bc4b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc4b-120">CommonParameters</span></span>
<span data-ttu-id="7bc4b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc4b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc4b-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bc4b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc4b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bc4b-123">INPUTS</span></span>

## <span data-ttu-id="7bc4b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bc4b-124">OUTPUTS</span></span>

### <span data-ttu-id="7bc4b-125">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="7bc4b-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7bc4b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bc4b-126">NOTES</span></span>

<span data-ttu-id="7bc4b-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7bc4b-127">ALIASES</span></span>

## <span data-ttu-id="7bc4b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bc4b-128">RELATED LINKS</span></span>

