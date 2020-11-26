---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262222"
---
# <span data-ttu-id="cf3b1-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cf3b1-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="cf3b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3b1-103">Ta bort databas huvud behörigheter.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="cf3b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf3b1-104">SYNTAX</span></span>

### <span data-ttu-id="cf3b1-105">RemoveExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="cf3b1-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3b1-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cf3b1-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf3b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf3b1-107">DESCRIPTION</span></span>
<span data-ttu-id="cf3b1-108">Ta bort databas huvud behörigheter.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="cf3b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf3b1-109">EXAMPLES</span></span>

### <span data-ttu-id="cf3b1-110">Exempel 1: ta bort behörigheter för databas säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="cf3b1-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="cf3b1-111">Kommandot ovan tar bort behörigheter för databas huvud gruppen</span><span class="sxs-lookup"><span data-stu-id="cf3b1-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="cf3b1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf3b1-112">PARAMETERS</span></span>

### <span data-ttu-id="cf3b1-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="cf3b1-113">-ClusterName</span></span>
<span data-ttu-id="cf3b1-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf3b1-115">-DatabaseName</span></span>
<span data-ttu-id="cf3b1-116">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3b1-117">-DefaultProfile</span></span>
<span data-ttu-id="cf3b1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf3b1-119">-InputObject</span></span>
<span data-ttu-id="cf3b1-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf3b1-122">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf3b1-123">-SubscriptionId</span></span>
<span data-ttu-id="cf3b1-124">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf3b1-125">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-126">-Värde</span><span class="sxs-lookup"><span data-stu-id="cf3b1-126">-Value</span></span>
<span data-ttu-id="cf3b1-127">Listan med Kusto databas säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="cf3b1-128">Om du vill skapa läser du avsnittet anteckningar för värde egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3b1-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf3b1-129">-Confirm</span></span>
<span data-ttu-id="cf3b1-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf3b1-131">-WhatIf</span></span>
<span data-ttu-id="cf3b1-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf3b1-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf3b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3b1-134">CommonParameters</span></span>
<span data-ttu-id="cf3b1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3b1-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf3b1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3b1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf3b1-137">INPUTS</span></span>

### <span data-ttu-id="cf3b1-138">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cf3b1-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cf3b1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf3b1-139">OUTPUTS</span></span>

### <span data-ttu-id="cf3b1-140">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cf3b1-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="cf3b1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf3b1-141">NOTES</span></span>

<span data-ttu-id="cf3b1-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cf3b1-142">ALIASES</span></span>

<span data-ttu-id="cf3b1-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cf3b1-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf3b1-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf3b1-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf3b1-146">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="cf3b1-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf3b1-147">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cf3b1-148">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cf3b1-149">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cf3b1-150">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cf3b1-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cf3b1-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf3b1-152">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cf3b1-153">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cf3b1-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cf3b1-155">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf3b1-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="cf3b1-157">VÄRDE <IDatabasePrincipal [] >: listan över Kusto-databasens säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="cf3b1-158">`Name <String>`: Databasens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="cf3b1-159">`Role <DatabasePrincipalRole>`: Rollen som databas huvud.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="cf3b1-160">`Type <DatabasePrincipalType>`: Databasens huvud typ.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="cf3b1-161">`[AppId <String>]`: Program-ID-relevant endast för program huvud typen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="cf3b1-162">`[Email <String>]`: E-postdatabasen om den finns.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="cf3b1-163">`[Fqn <String>]`: Ett fullständigt kvalificerat namn för databasen.</span><span class="sxs-lookup"><span data-stu-id="cf3b1-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="cf3b1-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf3b1-164">RELATED LINKS</span></span>
