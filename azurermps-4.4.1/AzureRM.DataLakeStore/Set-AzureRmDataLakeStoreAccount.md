---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756612"
---
# <span data-ttu-id="6af1e-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="6af1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6af1e-102">SYNOPSIS</span></span>
<span data-ttu-id="6af1e-103">Ändrar ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6af1e-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6af1e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6af1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6af1e-105">DESCRIPTION</span></span>
<span data-ttu-id="6af1e-106">Cmdleten **set-AzureRmDataLakeStoreAccount** ändrar ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6af1e-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="6af1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6af1e-107">EXAMPLES</span></span>

### <span data-ttu-id="6af1e-108">Exempel 1: lägga till en tagg till ett konto</span><span class="sxs-lookup"><span data-stu-id="6af1e-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="6af1e-109">Det här kommandot lägger till angiven tagg i kontot data Lake Store med namnet ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6af1e-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="6af1e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6af1e-110">PARAMETERS</span></span>

### <span data-ttu-id="6af1e-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="6af1e-111">-AllowAzureIpState</span></span>
<span data-ttu-id="6af1e-112">Tillåt/blockera Azure med IP-adresser via brand väggen.</span><span class="sxs-lookup"><span data-stu-id="6af1e-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="6af1e-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="6af1e-113">-DefaultGroup</span></span>
<span data-ttu-id="6af1e-114">Anger ID för en AzureActive.</span><span class="sxs-lookup"><span data-stu-id="6af1e-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="6af1e-115">Den här gruppen är standard gruppen för filer och mappar som du skapar.</span><span class="sxs-lookup"><span data-stu-id="6af1e-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="6af1e-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="6af1e-116">-FirewallState</span></span>
<span data-ttu-id="6af1e-117">Aktivera eller inaktivera befintliga brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="6af1e-117">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="6af1e-118">-Version</span><span class="sxs-lookup"><span data-stu-id="6af1e-118">-KeyVersion</span></span>
<span data-ttu-id="6af1e-119">Om krypterings typen är tilldelad användaren kan användaren rotera sin huvud version med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6af1e-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="6af1e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6af1e-120">-Name</span></span>
<span data-ttu-id="6af1e-121">Anger namnet på ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6af1e-121">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="6af1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6af1e-123">Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="6af1e-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="6af1e-124">-Taggar</span><span class="sxs-lookup"><span data-stu-id="6af1e-124">-Tags</span></span>
<span data-ttu-id="6af1e-125">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="6af1e-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="6af1e-126">Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="6af1e-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="6af1e-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="6af1e-127">-Tier</span></span>
<span data-ttu-id="6af1e-128">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="6af1e-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="6af1e-129">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="6af1e-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="6af1e-130">Alternativt kan du aktivera eller inaktivera befintliga betrodda ID-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="6af1e-130">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="6af1e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af1e-131">-DefaultProfile</span></span>
<span data-ttu-id="6af1e-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6af1e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af1e-133">CommonParameters</span></span>
<span data-ttu-id="6af1e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af1e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af1e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af1e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6af1e-136">INPUTS</span></span>

## <span data-ttu-id="6af1e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6af1e-137">OUTPUTS</span></span>

### <span data-ttu-id="6af1e-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="6af1e-139">Uppdaterade konto uppgifter.</span><span class="sxs-lookup"><span data-stu-id="6af1e-139">The updated account details.</span></span>

## <span data-ttu-id="6af1e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6af1e-140">NOTES</span></span>

## <span data-ttu-id="6af1e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6af1e-141">RELATED LINKS</span></span>

[<span data-ttu-id="6af1e-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6af1e-143">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6af1e-144">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6af1e-145">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6af1e-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


