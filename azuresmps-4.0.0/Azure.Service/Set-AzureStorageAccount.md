---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099080"
---
# <span data-ttu-id="0e71b-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e71b-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="0e71b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e71b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e71b-103">Uppdaterar egenskaperna för ett lagrings konto i en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0e71b-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="0e71b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e71b-104">SYNTAX</span></span>

### <span data-ttu-id="0e71b-105">Start"(standard)</span><span class="sxs-lookup"><span data-stu-id="0e71b-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0e71b-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="0e71b-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0e71b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e71b-107">DESCRIPTION</span></span>
<span data-ttu-id="0e71b-108">Cmdleten **set-AzureStorageAccount** uppdaterar egenskaperna för ett Azure Storage-konto i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0e71b-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="0e71b-109">Egenskaper som kan anges är: **etikett** , **Beskrivning** , **typ** och **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="0e71b-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="0e71b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e71b-110">EXAMPLES</span></span>

### <span data-ttu-id="0e71b-111">Exempel 1: uppdatera etiketten för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0e71b-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="0e71b-112">Det här kommandot uppdaterar egenskaperna **etikett** och **Beskrivning** för lagrings kontot som heter ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="0e71b-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="0e71b-113">Exempel 2: Aktivera geo-replikering för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0e71b-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="0e71b-114">Det här kommandot ställer in egenskapen **GeoReplicationEnabled** på $false för lagrings kontot med namnet ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="0e71b-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="0e71b-115">Exempel 3: inaktivera geo-replikering för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0e71b-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="0e71b-116">Det här kommandot ställer in egenskapen **GeoReplicationEnabled** på $True för lagrings kontot med namnet ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="0e71b-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="0e71b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e71b-117">PARAMETERS</span></span>

### <span data-ttu-id="0e71b-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0e71b-118">-Description</span></span>
<span data-ttu-id="0e71b-119">Anger en beskrivning av lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="0e71b-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="0e71b-120">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="0e71b-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="0e71b-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="0e71b-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="0e71b-122">Anger om lagrings kontot skapas med geo-replikering aktiverat.</span><span class="sxs-lookup"><span data-stu-id="0e71b-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e71b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0e71b-123">-InformationAction</span></span>
<span data-ttu-id="0e71b-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="0e71b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0e71b-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0e71b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e71b-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="0e71b-126">Continue</span></span>
- <span data-ttu-id="0e71b-127">Över</span><span class="sxs-lookup"><span data-stu-id="0e71b-127">Ignore</span></span>
- <span data-ttu-id="0e71b-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="0e71b-128">Inquire</span></span>
- <span data-ttu-id="0e71b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0e71b-129">SilentlyContinue</span></span>
- <span data-ttu-id="0e71b-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="0e71b-130">Stop</span></span>
- <span data-ttu-id="0e71b-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="0e71b-131">Suspend</span></span>

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

### <span data-ttu-id="0e71b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0e71b-132">-InformationVariable</span></span>
<span data-ttu-id="0e71b-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="0e71b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0e71b-134">-Etikett</span><span class="sxs-lookup"><span data-stu-id="0e71b-134">-Label</span></span>
<span data-ttu-id="0e71b-135">Anger en etikett för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="0e71b-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="0e71b-136">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="0e71b-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="0e71b-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="0e71b-137">-Profile</span></span>
<span data-ttu-id="0e71b-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0e71b-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e71b-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0e71b-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0e71b-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e71b-140">-StorageAccountName</span></span>
<span data-ttu-id="0e71b-141">Anger namnet på det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0e71b-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e71b-142">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0e71b-142">-Type</span></span>
<span data-ttu-id="0e71b-143">Anger typen av lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="0e71b-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="0e71b-144">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0e71b-144">Valid values are:</span></span> 

- <span data-ttu-id="0e71b-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="0e71b-145">Standard_LRS</span></span>
- <span data-ttu-id="0e71b-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="0e71b-146">Standard_ZRS</span></span>
- <span data-ttu-id="0e71b-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="0e71b-147">Standard_GRS</span></span>
- <span data-ttu-id="0e71b-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="0e71b-148">Standard_RAGRS</span></span>
- <span data-ttu-id="0e71b-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="0e71b-149">Premium_LRS</span></span>

<span data-ttu-id="0e71b-150">Om den här parametern inte anges är standardvärdet Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="0e71b-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="0e71b-151">Resultatet av att ange parametern *GeoReplicationEnabled* är detsamma som att ange Standard_GRS i parameter *typen* .</span><span class="sxs-lookup"><span data-stu-id="0e71b-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="0e71b-152">Standard_ZRS-eller Premium_LRS konton kan inte ändras till andra konto typer och vice versa.</span><span class="sxs-lookup"><span data-stu-id="0e71b-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e71b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e71b-153">CommonParameters</span></span>
<span data-ttu-id="0e71b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e71b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e71b-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e71b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e71b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e71b-156">INPUTS</span></span>

## <span data-ttu-id="0e71b-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e71b-157">OUTPUTS</span></span>

## <span data-ttu-id="0e71b-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e71b-158">NOTES</span></span>

## <span data-ttu-id="0e71b-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e71b-159">RELATED LINKS</span></span>

[<span data-ttu-id="0e71b-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e71b-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="0e71b-161">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e71b-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="0e71b-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e71b-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


