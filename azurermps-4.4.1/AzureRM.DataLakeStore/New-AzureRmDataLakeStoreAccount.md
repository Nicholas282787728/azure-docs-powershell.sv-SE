---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758413"
---
# <span data-ttu-id="a792f-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="a792f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a792f-102">SYNOPSIS</span></span>
<span data-ttu-id="a792f-103">Skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="a792f-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a792f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a792f-104">SYNTAX</span></span>

### <span data-ttu-id="a792f-105">Användare eller systemkopplad kryptering (standard)</span><span class="sxs-lookup"><span data-stu-id="a792f-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a792f-106">Inaktivera kryptering</span><span class="sxs-lookup"><span data-stu-id="a792f-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a792f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a792f-107">DESCRIPTION</span></span>
<span data-ttu-id="a792f-108">Cmdleten **New-AzureRmDataLakeStoreAccount** skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="a792f-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="a792f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a792f-109">EXAMPLES</span></span>

### <span data-ttu-id="a792f-110">Exempel 1: skapa ett konto</span><span class="sxs-lookup"><span data-stu-id="a792f-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="a792f-111">Det här kommandot skapar ett data Lake Store-konto med namnet ContosoADL för platsen östra USA 2.</span><span class="sxs-lookup"><span data-stu-id="a792f-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="a792f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a792f-112">PARAMETERS</span></span>

### <span data-ttu-id="a792f-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="a792f-113">-DefaultGroup</span></span>
<span data-ttu-id="a792f-114">Anger objekt-ID: t för den AzureActive som ska användas som standard grupp ägare för nya filer och mappar.</span><span class="sxs-lookup"><span data-stu-id="a792f-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="a792f-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="a792f-115">-DisableEncryption</span></span>
<span data-ttu-id="a792f-116">Visar att kontot inte har någon krypterings form.</span><span class="sxs-lookup"><span data-stu-id="a792f-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-117">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="a792f-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a792f-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a792f-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-120">-Version</span><span class="sxs-lookup"><span data-stu-id="a792f-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="a792f-121">-Location</span></span>
<span data-ttu-id="a792f-122">Anger platsen för kontot.</span><span class="sxs-lookup"><span data-stu-id="a792f-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="a792f-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a792f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a792f-124">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="a792f-124">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a792f-125">-Name</span></span>
<span data-ttu-id="a792f-126">Anger namnet på kontot som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a792f-126">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a792f-127">-ResourceGroupName</span></span>
<span data-ttu-id="a792f-128">Anger namnet på den resurs grupp som innehåller kontot.</span><span class="sxs-lookup"><span data-stu-id="a792f-128">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="a792f-129">-Taggar</span><span class="sxs-lookup"><span data-stu-id="a792f-129">-Tags</span></span>
<span data-ttu-id="a792f-130">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a792f-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="a792f-131">Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="a792f-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792f-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="a792f-132">-Tier</span></span>
<span data-ttu-id="a792f-133">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="a792f-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="a792f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a792f-134">-DefaultProfile</span></span>
<span data-ttu-id="a792f-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a792f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a792f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a792f-136">CommonParameters</span></span>
<span data-ttu-id="a792f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a792f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a792f-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a792f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a792f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a792f-139">INPUTS</span></span>

## <span data-ttu-id="a792f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a792f-140">OUTPUTS</span></span>

### <span data-ttu-id="a792f-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="a792f-142">De skapade konto uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="a792f-142">The created account details.</span></span>

## <span data-ttu-id="a792f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a792f-143">NOTES</span></span>

## <span data-ttu-id="a792f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a792f-144">RELATED LINKS</span></span>

[<span data-ttu-id="a792f-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a792f-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a792f-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a792f-148">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a792f-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


