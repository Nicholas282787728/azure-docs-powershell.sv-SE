---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c9964bfb6d9f701d88a16b8a227aec7c2018a217
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574301"
---
# <span data-ttu-id="abf8e-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="abf8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="abf8e-103">Skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="abf8e-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abf8e-104">SYNTAX</span></span>

### <span data-ttu-id="abf8e-105">UserOrSystemAssignedEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="abf8e-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf8e-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="abf8e-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf8e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abf8e-107">DESCRIPTION</span></span>
<span data-ttu-id="abf8e-108">Cmdleten **New-AzureRmDataLakeStoreAccount** skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="abf8e-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="abf8e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abf8e-109">EXAMPLES</span></span>

### <span data-ttu-id="abf8e-110">Exempel 1: skapa ett konto</span><span class="sxs-lookup"><span data-stu-id="abf8e-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="abf8e-111">Det här kommandot skapar ett data Lake Store-konto med namnet ContosoADL för platsen östra USA 2.</span><span class="sxs-lookup"><span data-stu-id="abf8e-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="abf8e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abf8e-112">PARAMETERS</span></span>

### <span data-ttu-id="abf8e-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="abf8e-113">-DefaultGroup</span></span>
<span data-ttu-id="abf8e-114">Anger objekt-ID: t för den AzureActive som ska användas som standard grupp ägare för nya filer och mappar.</span><span class="sxs-lookup"><span data-stu-id="abf8e-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf8e-115">-DefaultProfile</span></span>
<span data-ttu-id="abf8e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="abf8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="abf8e-117">-DisableEncryption</span></span>
<span data-ttu-id="abf8e-118">Visar att kontot inte har någon krypterings form.</span><span class="sxs-lookup"><span data-stu-id="abf8e-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-119">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="abf8e-119">-Encryption</span></span>
```yaml
Type: EncryptionConfigType
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="abf8e-120">-KeyName</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="abf8e-121">-KeyVaultId</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-122">-Version</span><span class="sxs-lookup"><span data-stu-id="abf8e-122">-KeyVersion</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="abf8e-123">-Location</span></span>
<span data-ttu-id="abf8e-124">Anger platsen för kontot.</span><span class="sxs-lookup"><span data-stu-id="abf8e-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="abf8e-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="abf8e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abf8e-126">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="abf8e-126">East US 2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="abf8e-127">-Name</span></span>
<span data-ttu-id="abf8e-128">Anger namnet på kontot som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="abf8e-128">Specifies the name of the account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf8e-129">-ResourceGroupName</span></span>
<span data-ttu-id="abf8e-130">Anger namnet på den resurs grupp som innehåller kontot.</span><span class="sxs-lookup"><span data-stu-id="abf8e-130">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abf8e-131">-Tag</span></span>
<span data-ttu-id="abf8e-132">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="abf8e-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="abf8e-133">Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="abf8e-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="abf8e-134">-Tier</span></span>
<span data-ttu-id="abf8e-135">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="abf8e-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf8e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf8e-136">CommonParameters</span></span>
<span data-ttu-id="abf8e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf8e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf8e-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf8e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf8e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abf8e-139">INPUTS</span></span>

### <span data-ttu-id="abf8e-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="abf8e-140">None</span></span>
<span data-ttu-id="abf8e-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="abf8e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abf8e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abf8e-142">OUTPUTS</span></span>

### <span data-ttu-id="abf8e-143">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-143">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="abf8e-144">De skapade konto uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="abf8e-144">The created account details.</span></span>

## <span data-ttu-id="abf8e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abf8e-145">NOTES</span></span>

## <span data-ttu-id="abf8e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abf8e-146">RELATED LINKS</span></span>

[<span data-ttu-id="abf8e-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="abf8e-148">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-148">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="abf8e-149">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-149">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="abf8e-150">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="abf8e-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


