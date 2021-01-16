---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403984"
---
# <span data-ttu-id="d61ce-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="d61ce-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="d61ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d61ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d61ce-103">Returnerar en lista över databasens huvud namn för det angivna Kusto-klustret och-databasen.</span><span class="sxs-lookup"><span data-stu-id="d61ce-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="d61ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d61ce-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d61ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d61ce-105">DESCRIPTION</span></span>
<span data-ttu-id="d61ce-106">Returnerar en lista över databasens huvud namn för det angivna Kusto-klustret och-databasen.</span><span class="sxs-lookup"><span data-stu-id="d61ce-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="d61ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d61ce-107">EXAMPLES</span></span>

### <span data-ttu-id="d61ce-108">Exempel 1: lista över databas huvud konton för angivet Kusto-kluster och databas</span><span class="sxs-lookup"><span data-stu-id="d61ce-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="d61ce-109">Kommandot ovan returnerar en lista över databasens huvud namn för angivet Kusto-kluster och-databas</span><span class="sxs-lookup"><span data-stu-id="d61ce-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="d61ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d61ce-110">PARAMETERS</span></span>

### <span data-ttu-id="d61ce-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d61ce-111">-ClusterName</span></span>
<span data-ttu-id="d61ce-112">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d61ce-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d61ce-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d61ce-113">-DatabaseName</span></span>
<span data-ttu-id="d61ce-114">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d61ce-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d61ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61ce-115">-DefaultProfile</span></span>
<span data-ttu-id="d61ce-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d61ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d61ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="d61ce-118">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d61ce-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d61ce-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d61ce-119">-SubscriptionId</span></span>
<span data-ttu-id="d61ce-120">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d61ce-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d61ce-121">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d61ce-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d61ce-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d61ce-122">-Confirm</span></span>
<span data-ttu-id="d61ce-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d61ce-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d61ce-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d61ce-124">-WhatIf</span></span>
<span data-ttu-id="d61ce-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d61ce-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d61ce-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d61ce-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d61ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61ce-127">CommonParameters</span></span>
<span data-ttu-id="d61ce-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61ce-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d61ce-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61ce-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d61ce-130">INPUTS</span></span>

## <span data-ttu-id="d61ce-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d61ce-131">OUTPUTS</span></span>

### <span data-ttu-id="d61ce-132">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="d61ce-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="d61ce-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d61ce-133">NOTES</span></span>

<span data-ttu-id="d61ce-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d61ce-134">ALIASES</span></span>

## <span data-ttu-id="d61ce-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d61ce-135">RELATED LINKS</span></span>

