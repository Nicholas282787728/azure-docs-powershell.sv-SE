---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916850"
---
# <span data-ttu-id="5ce0a-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5ce0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ce0a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce0a-103">Ändrar ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="5ce0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ce0a-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ce0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ce0a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce0a-106">Cmdleten **set-AzDataLakeStoreAccount** ändrar ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="5ce0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ce0a-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce0a-108">Exempel 1: lägga till en tagg till ett konto</span><span class="sxs-lookup"><span data-stu-id="5ce0a-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="5ce0a-109">Det här kommandot lägger till angiven tagg i kontot data Lake Store med namnet ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="5ce0a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ce0a-110">PARAMETERS</span></span>

### <span data-ttu-id="5ce0a-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="5ce0a-111">-AllowAzureIpState</span></span>
<span data-ttu-id="5ce0a-112">Tillåt/blockera Azure med IP-adresser via brand väggen.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="5ce0a-113">-DefaultGroup</span></span>
<span data-ttu-id="5ce0a-114">Anger ID för en AzureActive.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="5ce0a-115">Den här gruppen är standard gruppen för filer och mappar som du skapar.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce0a-116">-DefaultProfile</span></span>
<span data-ttu-id="5ce0a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5ce0a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ce0a-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="5ce0a-118">-FirewallState</span></span>
<span data-ttu-id="5ce0a-119">Aktivera eller inaktivera befintliga brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-120">-Version</span><span class="sxs-lookup"><span data-stu-id="5ce0a-120">-KeyVersion</span></span>
<span data-ttu-id="5ce0a-121">Om krypterings typen är tilldelad användaren kan användaren rotera sin huvud version med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ce0a-122">-Name</span></span>
<span data-ttu-id="5ce0a-123">Anger namnet på ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="5ce0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ce0a-125">Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5ce0a-126">-Tag</span></span>
<span data-ttu-id="5ce0a-127">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="5ce0a-128">Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="5ce0a-129">-Tier</span></span>
<span data-ttu-id="5ce0a-130">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="5ce0a-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="5ce0a-132">Alternativt kan du aktivera eller inaktivera befintliga betrodda ID-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce0a-133">CommonParameters</span></span>
<span data-ttu-id="5ce0a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce0a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce0a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce0a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ce0a-136">INPUTS</span></span>

### <span data-ttu-id="5ce0a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce0a-137">System.String</span></span>

### <span data-ttu-id="5ce0a-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5ce0a-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ce0a-139">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5ce0a-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5ce0a-140">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. FirewallState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5ce0a-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5ce0a-141">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. TierType, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5ce0a-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5ce0a-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5ce0a-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5ce0a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ce0a-143">OUTPUTS</span></span>

### <span data-ttu-id="5ce0a-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="5ce0a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ce0a-145">NOTES</span></span>

## <span data-ttu-id="5ce0a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ce0a-146">RELATED LINKS</span></span>

[<span data-ttu-id="5ce0a-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5ce0a-148">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5ce0a-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5ce0a-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5ce0a-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


