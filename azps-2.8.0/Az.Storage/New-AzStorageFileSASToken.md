---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: 9a0a25664a5512dcdecea268cff1e2cdc177d3dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919528"
---
# <span data-ttu-id="3bc0d-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3bc0d-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="3bc0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc0d-103">Genererar en signatur för en delad åtkomsttoken för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="3bc0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bc0d-104">SYNTAX</span></span>

### <span data-ttu-id="3bc0d-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="3bc0d-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc0d-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3bc0d-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc0d-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="3bc0d-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc0d-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3bc0d-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc0d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bc0d-109">DESCRIPTION</span></span>
<span data-ttu-id="3bc0d-110">**New-AzStorageFileSASToken-** cmdleten genererar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="3bc0d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bc0d-111">EXAMPLES</span></span>

### <span data-ttu-id="3bc0d-112">Exempel 1: generera ett signatur-token för delad åtkomst med fullständig fil behörighet</span><span class="sxs-lookup"><span data-stu-id="3bc0d-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="3bc0d-113">Det här kommandot skapar ett signatur-token för delad åtkomst som har fullständig behörighet till den fil som heter sökväg.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="3bc0d-114">Exempel 2: generera ett signatur-token för delad åtkomst med en tids gräns</span><span class="sxs-lookup"><span data-stu-id="3bc0d-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="3bc0d-115">Det första kommandot skapar ett **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="3bc0d-116">Kommandot lagrar den aktuella tiden i $StartTime variabeln.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="3bc0d-117">Det andra kommandot lägger till två timmar i objektet i $StartTime och lagrar sedan resultatet i $EndTime variabel.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="3bc0d-118">Det här objektet är en tid två timmar längre fram.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="3bc0d-119">Det tredje kommandot genererar en signatur för delad åtkomst med den angivna behörigheten.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="3bc0d-120">Denna token blir giltig för tillfället.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="3bc0d-121">Token är giltig tills tiden lagras i $EndTime.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="3bc0d-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bc0d-122">PARAMETERS</span></span>

### <span data-ttu-id="3bc0d-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3bc0d-123">-Context</span></span>
<span data-ttu-id="3bc0d-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3bc0d-125">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc0d-126">-DefaultProfile</span></span>
<span data-ttu-id="3bc0d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3bc0d-128">-ExpiryTime</span></span>
<span data-ttu-id="3bc0d-129">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-130">-Fil</span><span class="sxs-lookup"><span data-stu-id="3bc0d-130">-File</span></span>
<span data-ttu-id="3bc0d-131">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3bc0d-132">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3bc0d-133">-FullUri</span></span>
<span data-ttu-id="3bc0d-134">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3bc0d-135">-IPAddressOrRange</span></span>
<span data-ttu-id="3bc0d-136">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3bc0d-137">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-137">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3bc0d-138">-Path</span></span>
<span data-ttu-id="3bc0d-139">Anger sökvägen till filen i förhållande till en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-140">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3bc0d-140">-Permission</span></span>
<span data-ttu-id="3bc0d-141">Anger behörigheterna för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="3bc0d-142">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="3bc0d-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-143">-Princip</span><span class="sxs-lookup"><span data-stu-id="3bc0d-143">-Policy</span></span>
<span data-ttu-id="3bc0d-144">Anger den lagrade åtkomst principen för en fil.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3bc0d-145">-Protocol</span></span>
<span data-ttu-id="3bc0d-146">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3bc0d-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3bc0d-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3bc0d-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3bc0d-148">HttpsOnly</span></span>
* <span data-ttu-id="3bc0d-149">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3bc0d-150">-ShareName</span></span>
<span data-ttu-id="3bc0d-151">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3bc0d-152">-StartTime</span></span>
<span data-ttu-id="3bc0d-153">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-153">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc0d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc0d-154">CommonParameters</span></span>
<span data-ttu-id="3bc0d-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc0d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc0d-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc0d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc0d-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bc0d-157">INPUTS</span></span>

### <span data-ttu-id="3bc0d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc0d-158">System.String</span></span>

### <span data-ttu-id="3bc0d-159">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3bc0d-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3bc0d-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bc0d-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3bc0d-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bc0d-161">OUTPUTS</span></span>

### <span data-ttu-id="3bc0d-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc0d-162">System.String</span></span>

## <span data-ttu-id="3bc0d-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bc0d-163">NOTES</span></span>

## <span data-ttu-id="3bc0d-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bc0d-164">RELATED LINKS</span></span>

[<span data-ttu-id="3bc0d-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bc0d-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3bc0d-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="3bc0d-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
