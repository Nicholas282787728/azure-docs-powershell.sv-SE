---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093241"
---
# <span data-ttu-id="60e84-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="60e84-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="60e84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60e84-102">SYNOPSIS</span></span>
<span data-ttu-id="60e84-103">Förbereder ett nätverks konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="60e84-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="60e84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60e84-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60e84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60e84-105">DESCRIPTION</span></span>
<span data-ttu-id="60e84-106">Cmdleten **New-AzureStorSimpleNetworkConfig** förbereder ett nätverks konfigurations objekt för överföring till cmdleten **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="60e84-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="60e84-107">Ange parametern *Controller0IPAddress* och *Controller1IPAddress* för Data0-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="60e84-108">Data0 stöder bara tre inställningar: *Controller0IPAddress* , *Controller1IPAdress* och *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="60e84-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="60e84-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60e84-109">EXAMPLES</span></span>

### <span data-ttu-id="60e84-110">Exempel 1: Konfigurera ett Data0 gränssnitt</span><span class="sxs-lookup"><span data-stu-id="60e84-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="60e84-111">Det här kommandot skapar nätverks konfiguration för Data0-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="60e84-112">Det här kommandot anger parametrarna *Controller0IPv4Address* , *Controller1IPv4Address* och *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="60e84-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="60e84-113">Denna cmdlet kan konfigurera Data0 för endast dessa tre parametrar.</span><span class="sxs-lookup"><span data-stu-id="60e84-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="60e84-114">Exempel 2: Konfigurera ett annat gränssnitt än Data0 ett</span><span class="sxs-lookup"><span data-stu-id="60e84-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="60e84-115">Det här kommandot konfigurerar värdet data1.</span><span class="sxs-lookup"><span data-stu-id="60e84-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="60e84-116">Exempel 3: ändra en konfiguration för en enhet</span><span class="sxs-lookup"><span data-stu-id="60e84-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="60e84-117">Det första kommandot skapar en nätverks konfiguration för Data0-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="60e84-118">Det här kommandot anger parametrarna *Controller0IPv4Address* , *Controller1IPv4Address* och *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="60e84-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="60e84-119">Kommandot sparar resultatet i variabeln $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="60e84-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="60e84-120">I det andra kommandot används cmdleten **Get-AzureStorSimpleDevice** och en cmdlet för **WHERE-objekt** för att hämta en online StorSimple-enhet och sedan lagras den i $OnlineDevice variabel.</span><span class="sxs-lookup"><span data-stu-id="60e84-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="60e84-121">Det sista kommandot ändrar konfigurationen för enheten som har angivet enhets-ID genom att använda cmdleten **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="60e84-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="60e84-122">Kommandot använder det konfigurations objekt som den aktuella cmdleten skapade i det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="60e84-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="60e84-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60e84-123">PARAMETERS</span></span>

### <span data-ttu-id="60e84-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="60e84-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="60e84-125">Anger IPv4-adressen för Controller 0.</span><span class="sxs-lookup"><span data-stu-id="60e84-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="60e84-126">Ange endast den här parametern för Data0-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-126">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="60e84-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="60e84-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="60e84-128">Anger IPv4-adressen för styrenhet 1.</span><span class="sxs-lookup"><span data-stu-id="60e84-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="60e84-129">Ange endast den här parametern för Data0-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-129">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="60e84-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="60e84-130">-EnableCloud</span></span>
<span data-ttu-id="60e84-131">Anger om molnet ska aktivera gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e84-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="60e84-132">-EnableIscsi</span></span>
<span data-ttu-id="60e84-133">Anger om du vill aktivera Internet SCSI (ISCSI) för gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e84-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="60e84-134">-InterfaceAlias</span></span>
<span data-ttu-id="60e84-135">Anger gränssnitts Ali Aset för gränssnitt som denna cmdlet tillhandahåller inställningar för.</span><span class="sxs-lookup"><span data-stu-id="60e84-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="60e84-136">Giltiga värden är från Data0 till Data5.</span><span class="sxs-lookup"><span data-stu-id="60e84-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e84-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="60e84-137">-IPv4Address</span></span>
<span data-ttu-id="60e84-138">Anger IPv4-adressen för gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-138">Specifies the IPv4 address for the interface.</span></span>

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

### <span data-ttu-id="60e84-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="60e84-139">-IPv4Gateway</span></span>
<span data-ttu-id="60e84-140">Anger IPv4-adressen för en gateway.</span><span class="sxs-lookup"><span data-stu-id="60e84-140">Specifies the IPv4 address of a gateway.</span></span>

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

### <span data-ttu-id="60e84-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="60e84-141">-IPv4Netmask</span></span>
<span data-ttu-id="60e84-142">Anger gränssnittets IPv4-nätmask.</span><span class="sxs-lookup"><span data-stu-id="60e84-142">Specifies the IPv4 netmask for the interface.</span></span>

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

### <span data-ttu-id="60e84-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="60e84-143">-IPv6Gateway</span></span>
<span data-ttu-id="60e84-144">Anger IPv6-Gateway för gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-144">Specifies the IPv6 gateway for the interface.</span></span>

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

### <span data-ttu-id="60e84-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="60e84-145">-IPv6Prefix</span></span>
<span data-ttu-id="60e84-146">Anger IPv6-prefixet för gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60e84-146">Specifies the IPv6 prefix for the interface.</span></span>

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

### <span data-ttu-id="60e84-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="60e84-147">-Profile</span></span>
<span data-ttu-id="60e84-148">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="60e84-148">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="60e84-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e84-149">CommonParameters</span></span>
<span data-ttu-id="60e84-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e84-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e84-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e84-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e84-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60e84-152">INPUTS</span></span>

### <span data-ttu-id="60e84-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="60e84-153">None</span></span>

## <span data-ttu-id="60e84-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60e84-154">OUTPUTS</span></span>

### <span data-ttu-id="60e84-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="60e84-155">NetworkConfig</span></span>
<span data-ttu-id="60e84-156">Denna cmdlet returnerar ett NetworkConfig-objekt som innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="60e84-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="60e84-157">**IsIscsiEnabled** ( **boolesk** )</span><span class="sxs-lookup"><span data-stu-id="60e84-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="60e84-158">**IsCloudEnabled** ( **boolesk** )</span><span class="sxs-lookup"><span data-stu-id="60e84-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="60e84-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-163">**IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-164">**IPv6Prefix** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="60e84-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="60e84-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="60e84-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="60e84-166">**InterfaceAlias** ( **NetInterfaceId** )</span><span class="sxs-lookup"><span data-stu-id="60e84-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="60e84-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60e84-167">NOTES</span></span>

## <span data-ttu-id="60e84-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60e84-168">RELATED LINKS</span></span>

[<span data-ttu-id="60e84-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="60e84-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="60e84-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="60e84-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


