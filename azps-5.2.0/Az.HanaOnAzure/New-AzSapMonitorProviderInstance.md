---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392592"
---
# <span data-ttu-id="4cc98-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="4cc98-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="4cc98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cc98-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc98-103">Skapar en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4cc98-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="4cc98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cc98-104">SYNTAX</span></span>

### <span data-ttu-id="4cc98-105">ByString (standard)</span><span class="sxs-lookup"><span data-stu-id="4cc98-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4cc98-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="4cc98-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4cc98-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="4cc98-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4cc98-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cc98-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc98-109">Skapar en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4cc98-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="4cc98-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cc98-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc98-111">Exempel 1: skapa en instans av SAP Monitor by-sträng för HANA</span><span class="sxs-lookup"><span data-stu-id="4cc98-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-112">Det här kommandot skapar en instans av SAP Monitor by-strängen för HANA.</span><span class="sxs-lookup"><span data-stu-id="4cc98-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="4cc98-113">Exempel 2: skapa en instans av SAP monitor via Key valv för HANA</span><span class="sxs-lookup"><span data-stu-id="4cc98-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-114">Det här kommandot skapar en instans av SAP monitor via huvud valv för HANA.</span><span class="sxs-lookup"><span data-stu-id="4cc98-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="4cc98-115">Exempel 3: skapa en instans av SAP Monitor efter ord lista för PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="4cc98-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-116">Det här kommandot skapar en instans av SAP Monitor efter ord lista för PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="4cc98-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="4cc98-117">Exempel 4: skapa en instans av SAP Monitor efter ord lista för PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="4cc98-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-118">Det här kommandot skapar en instans av SAP Monitor efter ord lista för PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="4cc98-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="4cc98-119">Exempel 5: skapa en instans av SAP Monitor efter ord lista för MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="4cc98-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-120">Det här kommandot skapar en instans av SAP Monitor efter ord lista för MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="4cc98-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="4cc98-121">Exempel 6: skapa en instans av SAP Monitor efter ord lista för SapHana</span><span class="sxs-lookup"><span data-stu-id="4cc98-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4cc98-122">Det här kommandot skapar en instans av SAP Monitor efter ord lista för SapHana.</span><span class="sxs-lookup"><span data-stu-id="4cc98-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="4cc98-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cc98-123">PARAMETERS</span></span>

### <span data-ttu-id="4cc98-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cc98-124">-AsJob</span></span>
<span data-ttu-id="4cc98-125">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4cc98-125">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc98-126">-DefaultProfile</span></span>
<span data-ttu-id="4cc98-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc98-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cc98-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4cc98-128">-HanaDatabaseName</span></span>
<span data-ttu-id="4cc98-129">Databas namnet på SAP HANA-instans.</span><span class="sxs-lookup"><span data-stu-id="4cc98-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="4cc98-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="4cc98-131">Lösen ordet för databasen för SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="4cc98-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="4cc98-133">Resurs-ID för det huvud valv som innehåller HANA-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4cc98-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="4cc98-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="4cc98-135">Hemligt ID till nyckel valv hemligheten som innehåller HANA-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4cc98-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="4cc98-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="4cc98-137">SQL-porten för databasen hos SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="4cc98-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="4cc98-139">Användar namnet för databasen för SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="4cc98-140">-HanaHostname</span></span>
<span data-ttu-id="4cc98-141">Värd namnet för SAP HANA-instans.</span><span class="sxs-lookup"><span data-stu-id="4cc98-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="4cc98-142">-InstanceProperty</span></span>
<span data-ttu-id="4cc98-143">Egenskapen för HANA-förekomst.</span><span class="sxs-lookup"><span data-stu-id="4cc98-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4cc98-144">-Metadata</span></span>
<span data-ttu-id="4cc98-145">En JSON-sträng som innehåller metadata för tjänste instans.</span><span class="sxs-lookup"><span data-stu-id="4cc98-145">A JSON string containing metadata of the provider instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cc98-146">-Name</span></span>
<span data-ttu-id="4cc98-147">Namn på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4cc98-148">-NoWait</span></span>
<span data-ttu-id="4cc98-149">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4cc98-149">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="4cc98-150">-ProviderType</span></span>
<span data-ttu-id="4cc98-151">Typ av leverantörs instans.</span><span class="sxs-lookup"><span data-stu-id="4cc98-151">The type of provider instance.</span></span>
<span data-ttu-id="4cc98-152">Värden som stöds är: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="4cc98-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="4cc98-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc98-153">-ResourceGroupName</span></span>
<span data-ttu-id="4cc98-154">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="4cc98-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="4cc98-155">-SapMonitorName</span></span>
<span data-ttu-id="4cc98-156">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="4cc98-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cc98-157">-SubscriptionId</span></span>
<span data-ttu-id="4cc98-158">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4cc98-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4cc98-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4cc98-159">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc98-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cc98-160">-Confirm</span></span>
<span data-ttu-id="4cc98-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cc98-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc98-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc98-162">-WhatIf</span></span>
<span data-ttu-id="4cc98-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cc98-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc98-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cc98-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc98-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc98-165">CommonParameters</span></span>
<span data-ttu-id="4cc98-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc98-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc98-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cc98-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc98-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cc98-168">INPUTS</span></span>

## <span data-ttu-id="4cc98-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cc98-169">OUTPUTS</span></span>

### <span data-ttu-id="4cc98-170">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="4cc98-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="4cc98-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cc98-171">NOTES</span></span>

<span data-ttu-id="4cc98-172">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4cc98-172">ALIASES</span></span>

## <span data-ttu-id="4cc98-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cc98-173">RELATED LINKS</span></span>

