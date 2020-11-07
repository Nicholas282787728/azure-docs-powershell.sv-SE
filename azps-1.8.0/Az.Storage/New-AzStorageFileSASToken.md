---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: 7bb5f376953a378eadc2dee6b061ba3f876cfdf4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746334"
---
# <span data-ttu-id="d96ad-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="d96ad-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="d96ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d96ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d96ad-103">Genererar en signatur för en delad åtkomsttoken för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="d96ad-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="d96ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d96ad-104">SYNTAX</span></span>

### <span data-ttu-id="d96ad-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="d96ad-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d96ad-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="d96ad-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d96ad-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="d96ad-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d96ad-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="d96ad-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96ad-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d96ad-109">DESCRIPTION</span></span>
<span data-ttu-id="d96ad-110">**New-AzStorageFileSASToken-** cmdleten genererar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="d96ad-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="d96ad-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d96ad-111">EXAMPLES</span></span>

### <span data-ttu-id="d96ad-112">Exempel 1: generera ett signatur-token för delad åtkomst med fullständig fil behörighet</span><span class="sxs-lookup"><span data-stu-id="d96ad-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="d96ad-113">Det här kommandot skapar ett signatur-token för delad åtkomst som har fullständig behörighet till den fil som heter sökväg.</span><span class="sxs-lookup"><span data-stu-id="d96ad-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="d96ad-114">Exempel 2: generera ett signatur-token för delad åtkomst med en tids gräns</span><span class="sxs-lookup"><span data-stu-id="d96ad-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="d96ad-115">Det första kommandot skapar ett **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96ad-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="d96ad-116">Kommandot lagrar den aktuella tiden i $StartTime variabeln.</span><span class="sxs-lookup"><span data-stu-id="d96ad-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="d96ad-117">Det andra kommandot lägger till två timmar i objektet i $StartTime och lagrar sedan resultatet i $EndTime variabel.</span><span class="sxs-lookup"><span data-stu-id="d96ad-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="d96ad-118">Det här objektet är en tid två timmar längre fram.</span><span class="sxs-lookup"><span data-stu-id="d96ad-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="d96ad-119">Det tredje kommandot genererar en signatur för delad åtkomst med den angivna behörigheten.</span><span class="sxs-lookup"><span data-stu-id="d96ad-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="d96ad-120">Denna token blir giltig för tillfället.</span><span class="sxs-lookup"><span data-stu-id="d96ad-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="d96ad-121">Token är giltig tills tiden lagras i $EndTime.</span><span class="sxs-lookup"><span data-stu-id="d96ad-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="d96ad-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d96ad-122">PARAMETERS</span></span>

### <span data-ttu-id="d96ad-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d96ad-123">-Context</span></span>
<span data-ttu-id="d96ad-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="d96ad-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d96ad-125">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="d96ad-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d96ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96ad-126">-DefaultProfile</span></span>
<span data-ttu-id="d96ad-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d96ad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d96ad-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d96ad-128">-ExpiryTime</span></span>
<span data-ttu-id="d96ad-129">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="d96ad-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="d96ad-130">-Fil</span><span class="sxs-lookup"><span data-stu-id="d96ad-130">-File</span></span>
<span data-ttu-id="d96ad-131">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d96ad-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d96ad-132">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96ad-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d96ad-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d96ad-133">-FullUri</span></span>
<span data-ttu-id="d96ad-134">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d96ad-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d96ad-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d96ad-135">-IPAddressOrRange</span></span>
<span data-ttu-id="d96ad-136">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d96ad-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d96ad-137">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="d96ad-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="d96ad-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d96ad-138">-Path</span></span>
<span data-ttu-id="d96ad-139">Anger sökvägen till filen i förhållande till en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="d96ad-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="d96ad-140">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="d96ad-140">-Permission</span></span>
<span data-ttu-id="d96ad-141">Anger behörigheterna för en lagrings fil.</span><span class="sxs-lookup"><span data-stu-id="d96ad-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="d96ad-142">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="d96ad-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d96ad-143">-Princip</span><span class="sxs-lookup"><span data-stu-id="d96ad-143">-Policy</span></span>
<span data-ttu-id="d96ad-144">Anger den lagrade åtkomst principen för en fil.</span><span class="sxs-lookup"><span data-stu-id="d96ad-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="d96ad-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d96ad-145">-Protocol</span></span>
<span data-ttu-id="d96ad-146">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="d96ad-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d96ad-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d96ad-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d96ad-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d96ad-148">HttpsOnly</span></span>
* <span data-ttu-id="d96ad-149">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d96ad-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96ad-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d96ad-150">-ShareName</span></span>
<span data-ttu-id="d96ad-151">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="d96ad-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="d96ad-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d96ad-152">-StartTime</span></span>
<span data-ttu-id="d96ad-153">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="d96ad-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d96ad-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96ad-154">CommonParameters</span></span>
<span data-ttu-id="d96ad-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96ad-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96ad-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96ad-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96ad-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d96ad-157">INPUTS</span></span>

### <span data-ttu-id="d96ad-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d96ad-158">System.String</span></span>

### <span data-ttu-id="d96ad-159">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="d96ad-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="d96ad-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d96ad-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d96ad-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d96ad-161">OUTPUTS</span></span>

### <span data-ttu-id="d96ad-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d96ad-162">System.String</span></span>

## <span data-ttu-id="d96ad-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d96ad-163">NOTES</span></span>

## <span data-ttu-id="d96ad-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d96ad-164">RELATED LINKS</span></span>

[<span data-ttu-id="d96ad-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d96ad-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d96ad-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="d96ad-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
