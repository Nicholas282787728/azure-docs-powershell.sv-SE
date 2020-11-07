---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 052eae9a995aafe9d5d966ae5a17aae31a0fc0fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758307"
---
# <span data-ttu-id="c537f-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c537f-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="c537f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c537f-102">SYNOPSIS</span></span>
<span data-ttu-id="c537f-103">Genererar en signatur för en delad åtkomsttoken för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="c537f-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c537f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c537f-104">SYNTAX</span></span>

### <span data-ttu-id="c537f-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="c537f-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c537f-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="c537f-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c537f-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="c537f-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="c537f-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="c537f-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="c537f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c537f-109">DESCRIPTION</span></span>
<span data-ttu-id="c537f-110">**New-AzureStorageFileSASToken-** cmdleten genererar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="c537f-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="c537f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c537f-111">EXAMPLES</span></span>

### <span data-ttu-id="c537f-112">Exempel 1: generera ett signatur-token för delad åtkomst med fullständig fil behörighet</span><span class="sxs-lookup"><span data-stu-id="c537f-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="c537f-113">Det här kommandot skapar ett signatur-token för delad åtkomst som har fullständig behörighet till den fil som heter sökväg.</span><span class="sxs-lookup"><span data-stu-id="c537f-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="c537f-114">Exempel 2: generera ett signatur-token för delad åtkomst med en tids gräns</span><span class="sxs-lookup"><span data-stu-id="c537f-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="c537f-115">Det första kommandot skapar ett **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c537f-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="c537f-116">Kommandot lagrar den aktuella tiden i $StartTime variabeln.</span><span class="sxs-lookup"><span data-stu-id="c537f-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="c537f-117">Det andra kommandot lägger till två timmar i objektet i $StartTime och lagrar sedan resultatet i $EndTime variabel.</span><span class="sxs-lookup"><span data-stu-id="c537f-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="c537f-118">Det här objektet är en tid två timmar längre fram.</span><span class="sxs-lookup"><span data-stu-id="c537f-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="c537f-119">Det tredje kommandot genererar en signatur för delad åtkomst med den angivna behörigheten.</span><span class="sxs-lookup"><span data-stu-id="c537f-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="c537f-120">Denna token blir giltig för tillfället.</span><span class="sxs-lookup"><span data-stu-id="c537f-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="c537f-121">Token är giltig tills tiden lagras i $EndTime.</span><span class="sxs-lookup"><span data-stu-id="c537f-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="c537f-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c537f-122">PARAMETERS</span></span>

### <span data-ttu-id="c537f-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c537f-123">-Context</span></span>
<span data-ttu-id="c537f-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="c537f-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c537f-125">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="c537f-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c537f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c537f-126">-ExpiryTime</span></span>
<span data-ttu-id="c537f-127">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="c537f-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c537f-128">-Fil</span><span class="sxs-lookup"><span data-stu-id="c537f-128">-File</span></span>
<span data-ttu-id="c537f-129">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c537f-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c537f-130">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c537f-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="c537f-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c537f-131">-FullUri</span></span>
<span data-ttu-id="c537f-132">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="c537f-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c537f-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c537f-133">-IPAddressOrRange</span></span>
<span data-ttu-id="c537f-134">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c537f-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c537f-135">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="c537f-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="c537f-136">-Path</span><span class="sxs-lookup"><span data-stu-id="c537f-136">-Path</span></span>
<span data-ttu-id="c537f-137">Anger sökvägen till filen i förhållande till en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="c537f-137">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="c537f-138">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="c537f-138">-Permission</span></span>
<span data-ttu-id="c537f-139">Anger behörigheterna för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="c537f-139">Specifies the permissions for a Storage file.</span></span>

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

### <span data-ttu-id="c537f-140">-Princip</span><span class="sxs-lookup"><span data-stu-id="c537f-140">-Policy</span></span>
<span data-ttu-id="c537f-141">Anger den lagrade åtkomst principen för en fil.</span><span class="sxs-lookup"><span data-stu-id="c537f-141">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="c537f-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c537f-142">-Protocol</span></span>
<span data-ttu-id="c537f-143">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="c537f-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c537f-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c537f-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c537f-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c537f-145">HttpsOnly</span></span>
* <span data-ttu-id="c537f-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="c537f-146">HttpsOrHttp</span></span>

<span data-ttu-id="c537f-147">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c537f-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c537f-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c537f-148">-ShareName</span></span>
<span data-ttu-id="c537f-149">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="c537f-149">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="c537f-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c537f-150">-StartTime</span></span>
<span data-ttu-id="c537f-151">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="c537f-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c537f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c537f-152">CommonParameters</span></span>
<span data-ttu-id="c537f-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c537f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c537f-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c537f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c537f-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c537f-155">INPUTS</span></span>

### <span data-ttu-id="c537f-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c537f-156">IStorageContext</span></span>

<span data-ttu-id="c537f-157">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c537f-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c537f-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="c537f-158">CloudFile</span></span>

<span data-ttu-id="c537f-159">Parametern ' File ' godkänner värdet för typen ' CloudFile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c537f-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="c537f-160">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c537f-160">String</span></span>

<span data-ttu-id="c537f-161">Parametern ' path ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="c537f-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c537f-162">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c537f-162">String</span></span>

<span data-ttu-id="c537f-163">Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c537f-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c537f-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c537f-164">OUTPUTS</span></span>

### <span data-ttu-id="c537f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c537f-165">System.String</span></span>

## <span data-ttu-id="c537f-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c537f-166">NOTES</span></span>

## <span data-ttu-id="c537f-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c537f-167">RELATED LINKS</span></span>

[<span data-ttu-id="c537f-168">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c537f-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c537f-169">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c537f-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
