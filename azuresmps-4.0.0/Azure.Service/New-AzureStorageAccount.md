---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099434"
---
# <span data-ttu-id="cffbb-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cffbb-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="cffbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cffbb-102">SYNOPSIS</span></span>
<span data-ttu-id="cffbb-103">Skapar ett nytt lagrings konto i en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="cffbb-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="cffbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cffbb-104">SYNTAX</span></span>

### <span data-ttu-id="cffbb-105">ParameterSetAffinityGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="cffbb-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cffbb-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="cffbb-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cffbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cffbb-107">DESCRIPTION</span></span>
<span data-ttu-id="cffbb-108">**New-AzureStorageAccount** cmdlet skapar ett konto som ger åtkomst till Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="cffbb-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="cffbb-109">Ett lagrings konto är en globalt unik resurs i lagrings systemet.</span><span class="sxs-lookup"><span data-stu-id="cffbb-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="cffbb-110">Kontot är det överordnade namn området för BLOB-, kö-och tabell tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="cffbb-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="cffbb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cffbb-111">EXAMPLES</span></span>

### <span data-ttu-id="cffbb-112">Exempel 1: skapa ett lagrings konto för en angiven tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="cffbb-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="cffbb-113">Det här kommandot skapar ett lagrings konto för en angiven tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="cffbb-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="cffbb-114">Exempel 2: skapa ett lagrings konto på en angiven plats</span><span class="sxs-lookup"><span data-stu-id="cffbb-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="cffbb-115">Det här kommandot skapar ett lagrings konto på en angiven plats.</span><span class="sxs-lookup"><span data-stu-id="cffbb-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="cffbb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cffbb-116">PARAMETERS</span></span>

### <span data-ttu-id="cffbb-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="cffbb-117">-AffinityGroup</span></span>
<span data-ttu-id="cffbb-118">Anger namnet på en befintlig tillhörighets grupp i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cffbb-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="cffbb-119">Du kan ange parametern *plats* eller *AffinityGroup* , men inte båda.</span><span class="sxs-lookup"><span data-stu-id="cffbb-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cffbb-120">-Description</span></span>
<span data-ttu-id="cffbb-121">Anger en beskrivning av lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cffbb-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="cffbb-122">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="cffbb-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cffbb-123">-InformationAction</span></span>
<span data-ttu-id="cffbb-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="cffbb-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cffbb-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cffbb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cffbb-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="cffbb-126">Continue</span></span>
- <span data-ttu-id="cffbb-127">Över</span><span class="sxs-lookup"><span data-stu-id="cffbb-127">Ignore</span></span>
- <span data-ttu-id="cffbb-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="cffbb-128">Inquire</span></span>
- <span data-ttu-id="cffbb-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cffbb-129">SilentlyContinue</span></span>
- <span data-ttu-id="cffbb-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="cffbb-130">Stop</span></span>
- <span data-ttu-id="cffbb-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="cffbb-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cffbb-132">-InformationVariable</span></span>
<span data-ttu-id="cffbb-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="cffbb-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-134">-Etikett</span><span class="sxs-lookup"><span data-stu-id="cffbb-134">-Label</span></span>
<span data-ttu-id="cffbb-135">Anger en etikett för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cffbb-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="cffbb-136">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="cffbb-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="cffbb-137">-Location</span></span>
<span data-ttu-id="cffbb-138">Anger den Azure Data Center-plats där lagrings kontot skapas.</span><span class="sxs-lookup"><span data-stu-id="cffbb-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="cffbb-139">Du kan ta med parametern *location* eller *AffinityGroup* , men inte båda.</span><span class="sxs-lookup"><span data-stu-id="cffbb-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="cffbb-140">-Profile</span></span>
<span data-ttu-id="cffbb-141">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="cffbb-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cffbb-142">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cffbb-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cffbb-143">-StorageAccountName</span></span>
<span data-ttu-id="cffbb-144">Anger ett namn för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cffbb-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="cffbb-145">Lagrings konto namnet måste vara unikt för Azure och måste vara mellan 3 och 24 tecken långt och bara använda gemener och siffror.</span><span class="sxs-lookup"><span data-stu-id="cffbb-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-146">– Skriv</span><span class="sxs-lookup"><span data-stu-id="cffbb-146">-Type</span></span>
<span data-ttu-id="cffbb-147">Anger typen av lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="cffbb-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="cffbb-148">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="cffbb-148">Valid values are:</span></span>

- <span data-ttu-id="cffbb-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="cffbb-149">Standard_LRS</span></span>
- <span data-ttu-id="cffbb-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="cffbb-150">Standard_ZRS</span></span>
- <span data-ttu-id="cffbb-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="cffbb-151">Standard_GRS</span></span>
- <span data-ttu-id="cffbb-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="cffbb-152">Standard_RAGRS</span></span>
- <span data-ttu-id="cffbb-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="cffbb-153">Premium_LRS</span></span>

<span data-ttu-id="cffbb-154">Om den här parametern inte anges är standardvärdet Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="cffbb-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="cffbb-155">Standard_ZRS-eller Premium_LRS konton kan inte ändras till andra konto typer och vice versa.</span><span class="sxs-lookup"><span data-stu-id="cffbb-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffbb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffbb-156">CommonParameters</span></span>
<span data-ttu-id="cffbb-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cffbb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffbb-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffbb-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffbb-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cffbb-159">INPUTS</span></span>

## <span data-ttu-id="cffbb-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cffbb-160">OUTPUTS</span></span>

## <span data-ttu-id="cffbb-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cffbb-161">NOTES</span></span>

## <span data-ttu-id="cffbb-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cffbb-162">RELATED LINKS</span></span>

[<span data-ttu-id="cffbb-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cffbb-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="cffbb-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cffbb-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


