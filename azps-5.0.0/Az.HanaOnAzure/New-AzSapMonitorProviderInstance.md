---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263066"
---
# <span data-ttu-id="a4d9d-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a4d9d-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="a4d9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d9d-103">Skapar en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a4d9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4d9d-104">SYNTAX</span></span>

### <span data-ttu-id="a4d9d-105">ByString (standard)</span><span class="sxs-lookup"><span data-stu-id="a4d9d-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a4d9d-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="a4d9d-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4d9d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="a4d9d-108">Skapar en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a4d9d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4d9d-109">EXAMPLES</span></span>

### <span data-ttu-id="a4d9d-110">Exempel 1: skapa en instans av SAP Monitor by-sträng för HANA</span><span class="sxs-lookup"><span data-stu-id="a4d9d-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a4d9d-111">Det här kommandot skapar en instans av SAP Monitor by-strängen för HANA.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="a4d9d-112">Exempel 2: skapa en instans av SAP monitor via Key valv för HANA</span><span class="sxs-lookup"><span data-stu-id="a4d9d-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a4d9d-113">Det här kommandot skapar en instans av SAP monitor via huvud valv för HANA.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="a4d9d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4d9d-114">PARAMETERS</span></span>

### <span data-ttu-id="a4d9d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4d9d-115">-AsJob</span></span>
<span data-ttu-id="a4d9d-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a4d9d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a4d9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d9d-117">-DefaultProfile</span></span>
<span data-ttu-id="a4d9d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d9d-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4d9d-119">-HanaDatabaseName</span></span>
<span data-ttu-id="a4d9d-120">Databas namnet på SAP HANA-instans.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d9d-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="a4d9d-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="a4d9d-122">Lösen ordet för databasen för SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a4d9d-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="a4d9d-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="a4d9d-124">Resurs-ID för det huvud valv som innehåller HANA-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="a4d9d-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="a4d9d-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="a4d9d-126">Hemligt ID till nyckel valv hemligheten som innehåller HANA-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="a4d9d-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="a4d9d-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="a4d9d-128">SQL-porten för databasen hos SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d9d-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="a4d9d-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="a4d9d-130">Användar namnet för databasen för SAP HANA-instansen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d9d-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="a4d9d-131">-HanaHostname</span></span>
<span data-ttu-id="a4d9d-132">Värd namnet för SAP HANA-instans.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a4d9d-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a4d9d-133">-Metadata</span></span>
<span data-ttu-id="a4d9d-134">En JSON-sträng som innehåller metadata för tjänste instans.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="a4d9d-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4d9d-135">-Name</span></span>
<span data-ttu-id="a4d9d-136">Namn på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="a4d9d-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a4d9d-137">-NoWait</span></span>
<span data-ttu-id="a4d9d-138">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a4d9d-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a4d9d-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="a4d9d-139">-ProviderType</span></span>
<span data-ttu-id="a4d9d-140">Typ av leverantörs instans.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-140">The type of provider instance.</span></span>
<span data-ttu-id="a4d9d-141">Värden som stöds är: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="a4d9d-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="a4d9d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d9d-142">-ResourceGroupName</span></span>
<span data-ttu-id="a4d9d-143">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="a4d9d-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="a4d9d-144">-SapMonitorName</span></span>
<span data-ttu-id="a4d9d-145">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="a4d9d-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4d9d-146">-SubscriptionId</span></span>
<span data-ttu-id="a4d9d-147">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4d9d-148">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4d9d-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4d9d-149">-Confirm</span></span>
<span data-ttu-id="a4d9d-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d9d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d9d-151">-WhatIf</span></span>
<span data-ttu-id="a4d9d-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d9d-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d9d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d9d-154">CommonParameters</span></span>
<span data-ttu-id="a4d9d-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d9d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d9d-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4d9d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d9d-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4d9d-157">INPUTS</span></span>

## <span data-ttu-id="a4d9d-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4d9d-158">OUTPUTS</span></span>

### <span data-ttu-id="a4d9d-159">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a4d9d-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="a4d9d-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4d9d-160">NOTES</span></span>

<span data-ttu-id="a4d9d-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a4d9d-161">ALIASES</span></span>

## <span data-ttu-id="a4d9d-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4d9d-162">RELATED LINKS</span></span>

