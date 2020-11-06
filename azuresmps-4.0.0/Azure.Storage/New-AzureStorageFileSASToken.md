---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572020"
---
# <span data-ttu-id="1b165-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1b165-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="1b165-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b165-102">SYNOPSIS</span></span>
<span data-ttu-id="1b165-103">Genererar en signatur för en delad åtkomsttoken för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="1b165-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="1b165-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b165-104">SYNTAX</span></span>

### <span data-ttu-id="1b165-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="1b165-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1b165-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1b165-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1b165-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="1b165-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="1b165-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1b165-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="1b165-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b165-109">DESCRIPTION</span></span>
<span data-ttu-id="1b165-110">**New-AzureStorageFileSASToken-** cmdleten genererar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="1b165-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="1b165-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b165-111">EXAMPLES</span></span>

### <span data-ttu-id="1b165-112">Exempel 1: generera ett signatur-token för delad åtkomst med fullständig fil behörighet</span><span class="sxs-lookup"><span data-stu-id="1b165-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="1b165-113">Det här kommandot skapar ett signatur-token för delad åtkomst som har fullständig behörighet till den fil som heter sökväg.</span><span class="sxs-lookup"><span data-stu-id="1b165-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="1b165-114">Exempel 2: generera ett signatur-token för delad åtkomst med en tids gräns</span><span class="sxs-lookup"><span data-stu-id="1b165-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="1b165-115">Det första kommandot skapar ett **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b165-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1b165-116">Kommandot lagrar den aktuella tiden i $StartTime variabeln.</span><span class="sxs-lookup"><span data-stu-id="1b165-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="1b165-117">Det andra kommandot lägger till två timmar i objektet i $StartTime och lagrar sedan resultatet i $EndTime variabel.</span><span class="sxs-lookup"><span data-stu-id="1b165-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="1b165-118">Det här objektet är en tid två timmar längre fram.</span><span class="sxs-lookup"><span data-stu-id="1b165-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="1b165-119">Det tredje kommandot genererar en signatur för delad åtkomst med den angivna behörigheten.</span><span class="sxs-lookup"><span data-stu-id="1b165-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="1b165-120">Denna token blir giltig för tillfället.</span><span class="sxs-lookup"><span data-stu-id="1b165-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="1b165-121">Token är giltig tills tiden lagras i $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1b165-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="1b165-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b165-122">PARAMETERS</span></span>

### <span data-ttu-id="1b165-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1b165-123">-Context</span></span>
<span data-ttu-id="1b165-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="1b165-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1b165-125">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="1b165-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1b165-126">-ExpiryTime</span></span>
<span data-ttu-id="1b165-127">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="1b165-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-128">-Fil</span><span class="sxs-lookup"><span data-stu-id="1b165-128">-File</span></span>
<span data-ttu-id="1b165-129">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1b165-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1b165-130">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b165-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1b165-131">-FullUri</span></span>
<span data-ttu-id="1b165-132">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1b165-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1b165-133">-IPAddressOrRange</span></span>
<span data-ttu-id="1b165-134">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="1b165-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1b165-135">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="1b165-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="1b165-136">-Path</span><span class="sxs-lookup"><span data-stu-id="1b165-136">-Path</span></span>
<span data-ttu-id="1b165-137">Anger sökvägen till filen i förhållande till en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="1b165-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-138">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="1b165-138">-Permission</span></span>
<span data-ttu-id="1b165-139">Anger behörigheterna för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="1b165-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-140">-Princip</span><span class="sxs-lookup"><span data-stu-id="1b165-140">-Policy</span></span>
<span data-ttu-id="1b165-141">Anger den lagrade åtkomst principen för en fil.</span><span class="sxs-lookup"><span data-stu-id="1b165-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1b165-142">-Protocol</span></span>
<span data-ttu-id="1b165-143">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="1b165-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1b165-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b165-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1b165-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1b165-145">HttpsOnly</span></span>
* <span data-ttu-id="1b165-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1b165-146">HttpsOrHttp</span></span>

<span data-ttu-id="1b165-147">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1b165-147">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1b165-148">-ShareName</span></span>
<span data-ttu-id="1b165-149">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="1b165-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1b165-150">-StartTime</span></span>
<span data-ttu-id="1b165-151">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="1b165-151">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b165-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b165-152">CommonParameters</span></span>
<span data-ttu-id="1b165-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b165-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b165-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b165-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b165-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b165-155">INPUTS</span></span>

## <span data-ttu-id="1b165-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b165-156">OUTPUTS</span></span>

## <span data-ttu-id="1b165-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b165-157">NOTES</span></span>

## <span data-ttu-id="1b165-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b165-158">RELATED LINKS</span></span>

[<span data-ttu-id="1b165-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b165-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1b165-160">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1b165-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
