---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272242"
---
# <span data-ttu-id="1d52d-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d52d-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="1d52d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d52d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d52d-103">Returnerar en lista över databasens huvud namn för det angivna Kusto-klustret och-databasen.</span><span class="sxs-lookup"><span data-stu-id="1d52d-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="1d52d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d52d-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1d52d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d52d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d52d-106">Returnerar en lista över databasens huvud namn för det angivna Kusto-klustret och-databasen.</span><span class="sxs-lookup"><span data-stu-id="1d52d-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="1d52d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d52d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d52d-108">Exempel 1: lista över databas huvud konton för angivet Kusto-kluster och databas</span><span class="sxs-lookup"><span data-stu-id="1d52d-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="1d52d-109">Kommandot ovan returnerar en lista över databasens huvud namn för angivet Kusto-kluster och-databas</span><span class="sxs-lookup"><span data-stu-id="1d52d-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="1d52d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d52d-110">PARAMETERS</span></span>

### <span data-ttu-id="1d52d-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="1d52d-111">-ClusterName</span></span>
<span data-ttu-id="1d52d-112">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1d52d-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1d52d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d52d-113">-DatabaseName</span></span>
<span data-ttu-id="1d52d-114">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1d52d-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1d52d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d52d-115">-DefaultProfile</span></span>
<span data-ttu-id="1d52d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d52d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d52d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d52d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d52d-118">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1d52d-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1d52d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d52d-119">-SubscriptionId</span></span>
<span data-ttu-id="1d52d-120">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1d52d-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1d52d-121">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1d52d-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1d52d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d52d-122">-Confirm</span></span>
<span data-ttu-id="1d52d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d52d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d52d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d52d-124">-WhatIf</span></span>
<span data-ttu-id="1d52d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d52d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d52d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d52d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d52d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d52d-127">CommonParameters</span></span>
<span data-ttu-id="1d52d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d52d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d52d-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d52d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d52d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d52d-130">INPUTS</span></span>

## <span data-ttu-id="1d52d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d52d-131">OUTPUTS</span></span>

### <span data-ttu-id="1d52d-132">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d52d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="1d52d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d52d-133">NOTES</span></span>

<span data-ttu-id="1d52d-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1d52d-134">ALIASES</span></span>

## <span data-ttu-id="1d52d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d52d-135">RELATED LINKS</span></span>

