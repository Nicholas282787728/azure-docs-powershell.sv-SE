---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 3a3e2ea1fdac71759de7278ed34666e3a756ccca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572819"
---
# <span data-ttu-id="89f26-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="89f26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89f26-102">SYNOPSIS</span></span>
<span data-ttu-id="89f26-103">Skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="89f26-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89f26-104">SYNTAX</span></span>

### <span data-ttu-id="89f26-105">UserOrSystemAssignedEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="89f26-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89f26-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="89f26-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89f26-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89f26-107">DESCRIPTION</span></span>
<span data-ttu-id="89f26-108">Cmdleten **New-AzureRmDataLakeStoreAccount** skapar ett nytt data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="89f26-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="89f26-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89f26-109">EXAMPLES</span></span>

### <span data-ttu-id="89f26-110">Exempel 1: skapa ett konto</span><span class="sxs-lookup"><span data-stu-id="89f26-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="89f26-111">Det här kommandot skapar ett data Lake Store-konto med namnet ContosoADL för platsen östra USA 2.</span><span class="sxs-lookup"><span data-stu-id="89f26-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="89f26-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89f26-112">PARAMETERS</span></span>

### <span data-ttu-id="89f26-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="89f26-113">-DefaultGroup</span></span>
<span data-ttu-id="89f26-114">Anger objekt-ID: t för den AzureActive som ska användas som standard grupp ägare för nya filer och mappar.</span><span class="sxs-lookup"><span data-stu-id="89f26-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="89f26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f26-115">-DefaultProfile</span></span>
<span data-ttu-id="89f26-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="89f26-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f26-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="89f26-117">-DisableEncryption</span></span>
<span data-ttu-id="89f26-118">Visar att kontot inte har någon krypterings form.</span><span class="sxs-lookup"><span data-stu-id="89f26-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-119">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="89f26-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="89f26-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="89f26-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-122">-Version</span><span class="sxs-lookup"><span data-stu-id="89f26-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="89f26-123">-Location</span></span>
<span data-ttu-id="89f26-124">Anger platsen för kontot.</span><span class="sxs-lookup"><span data-stu-id="89f26-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="89f26-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="89f26-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89f26-126">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="89f26-126">East US 2</span></span>

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

### <span data-ttu-id="89f26-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="89f26-127">-Name</span></span>
<span data-ttu-id="89f26-128">Anger namnet på kontot som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="89f26-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="89f26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f26-129">-ResourceGroupName</span></span>
<span data-ttu-id="89f26-130">Anger namnet på den resurs grupp som innehåller kontot.</span><span class="sxs-lookup"><span data-stu-id="89f26-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="89f26-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="89f26-131">-Tag</span></span>
<span data-ttu-id="89f26-132">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="89f26-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="89f26-133">Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="89f26-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f26-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="89f26-134">-Tier</span></span>
<span data-ttu-id="89f26-135">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="89f26-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="89f26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f26-136">CommonParameters</span></span>
<span data-ttu-id="89f26-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f26-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f26-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f26-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89f26-139">INPUTS</span></span>

### <span data-ttu-id="89f26-140">System. String</span><span class="sxs-lookup"><span data-stu-id="89f26-140">System.String</span></span>

### <span data-ttu-id="89f26-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="89f26-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="89f26-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. EncryptionConfigType, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="89f26-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="89f26-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89f26-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="89f26-144">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. TierType, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="89f26-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="89f26-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89f26-145">OUTPUTS</span></span>

### <span data-ttu-id="89f26-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="89f26-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89f26-147">NOTES</span></span>

## <span data-ttu-id="89f26-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89f26-148">RELATED LINKS</span></span>

[<span data-ttu-id="89f26-149">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-149">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="89f26-150">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-150">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="89f26-151">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-151">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="89f26-152">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="89f26-152">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


