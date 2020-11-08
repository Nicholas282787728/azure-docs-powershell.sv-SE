---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099469"
---
# <span data-ttu-id="587d7-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="587d7-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="587d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="587d7-102">SYNOPSIS</span></span>
<span data-ttu-id="587d7-103">Migrerar ett lagrings konto till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="587d7-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="587d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="587d7-104">SYNTAX</span></span>

### <span data-ttu-id="587d7-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="587d7-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="587d7-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="587d7-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="587d7-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="587d7-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="587d7-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="587d7-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="587d7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="587d7-109">DESCRIPTION</span></span>
<span data-ttu-id="587d7-110">Cmdleten **Move-AzureStorageAccount** migrerar ett lagrings konto till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="587d7-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="587d7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="587d7-111">EXAMPLES</span></span>

### <span data-ttu-id="587d7-112">Exempel 1: Förbereda migrering av lagrings konto</span><span class="sxs-lookup"><span data-stu-id="587d7-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="587d7-113">Det här kommandot förbereder lagrings kontot med namnet ContosoStorageName för migrering till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="587d7-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="587d7-114">Exempel 2: starta migrering av lagrings konto</span><span class="sxs-lookup"><span data-stu-id="587d7-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="587d7-115">Det här kommandot startar migrering av lagrings kontot med namnet ContosoStorageName till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="587d7-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="587d7-116">Exempel 3: verifiera migrering av lagrings konto</span><span class="sxs-lookup"><span data-stu-id="587d7-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="587d7-117">Det här kommandot verifierar migrering för lagrings kontot med namnet ContosoStorageName till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="587d7-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="587d7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="587d7-118">PARAMETERS</span></span>

### <span data-ttu-id="587d7-119">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="587d7-119">-Abort</span></span>
<span data-ttu-id="587d7-120">Anger att denna cmdlet avbryter lagrings konto överflyttningen.</span><span class="sxs-lookup"><span data-stu-id="587d7-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587d7-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="587d7-121">-Commit</span></span>
<span data-ttu-id="587d7-122">Anger att denna cmdlet startar lagrings konto överflyttningen.</span><span class="sxs-lookup"><span data-stu-id="587d7-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587d7-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="587d7-123">-InformationAction</span></span>
<span data-ttu-id="587d7-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="587d7-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="587d7-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="587d7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="587d7-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="587d7-126">Continue</span></span>
- <span data-ttu-id="587d7-127">Över</span><span class="sxs-lookup"><span data-stu-id="587d7-127">Ignore</span></span>
- <span data-ttu-id="587d7-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="587d7-128">Inquire</span></span>
- <span data-ttu-id="587d7-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="587d7-129">SilentlyContinue</span></span>
- <span data-ttu-id="587d7-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="587d7-130">Stop</span></span>
- <span data-ttu-id="587d7-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="587d7-131">Suspend</span></span>

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

### <span data-ttu-id="587d7-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="587d7-132">-InformationVariable</span></span>
<span data-ttu-id="587d7-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="587d7-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="587d7-134">-Förbered</span><span class="sxs-lookup"><span data-stu-id="587d7-134">-Prepare</span></span>
<span data-ttu-id="587d7-135">Anger att denna cmdlet förbereder lagrings kontot för migrering.</span><span class="sxs-lookup"><span data-stu-id="587d7-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587d7-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="587d7-136">-Profile</span></span>
<span data-ttu-id="587d7-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="587d7-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="587d7-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="587d7-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="587d7-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="587d7-139">-StorageAccountName</span></span>
<span data-ttu-id="587d7-140">Anger namnet på det lagrings konto som denna cmdlet migrerar.</span><span class="sxs-lookup"><span data-stu-id="587d7-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="587d7-141">-Validera</span><span class="sxs-lookup"><span data-stu-id="587d7-141">-Validate</span></span>
<span data-ttu-id="587d7-142">Anger att lagrings kontot verifieras i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="587d7-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587d7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587d7-143">CommonParameters</span></span>
<span data-ttu-id="587d7-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587d7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587d7-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587d7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587d7-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="587d7-146">INPUTS</span></span>

## <span data-ttu-id="587d7-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="587d7-147">OUTPUTS</span></span>

## <span data-ttu-id="587d7-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="587d7-148">NOTES</span></span>

## <span data-ttu-id="587d7-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="587d7-149">RELATED LINKS</span></span>

[<span data-ttu-id="587d7-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="587d7-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="587d7-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="587d7-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="587d7-152">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="587d7-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="587d7-153">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="587d7-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="587d7-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="587d7-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


