---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925226"
---
# <span data-ttu-id="2480f-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="2480f-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="2480f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2480f-102">SYNOPSIS</span></span>
<span data-ttu-id="2480f-103">Hämtar en. RDP-fil.</span><span class="sxs-lookup"><span data-stu-id="2480f-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="2480f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2480f-104">SYNTAX</span></span>

### <span data-ttu-id="2480f-105">Bar</span><span class="sxs-lookup"><span data-stu-id="2480f-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2480f-106">Start</span><span class="sxs-lookup"><span data-stu-id="2480f-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2480f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2480f-107">DESCRIPTION</span></span>
<span data-ttu-id="2480f-108">Cmdleten **Get-AzRemoteDesktopFile** hämtar en RDP-fil (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="2480f-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="2480f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2480f-109">EXAMPLES</span></span>

### <span data-ttu-id="2480f-110">Exempel 1: Hämta en fjärr skrivbords fil</span><span class="sxs-lookup"><span data-stu-id="2480f-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="2480f-111">Det här kommandot får fjärr skrivbords filen för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="2480f-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2480f-112">Kommandot sparar resultatet i filen med namnet D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="2480f-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="2480f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2480f-113">PARAMETERS</span></span>

### <span data-ttu-id="2480f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2480f-114">-DefaultProfile</span></span>
<span data-ttu-id="2480f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2480f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2480f-116">-Lansera</span><span class="sxs-lookup"><span data-stu-id="2480f-116">-Launch</span></span>
<span data-ttu-id="2480f-117">Anger att denna cmdlet startar fjärr skrivbord när den får. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="2480f-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2480f-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="2480f-118">-LocalPath</span></span>
<span data-ttu-id="2480f-119">Anger lokal fullständig sökväg där denna cmdlet lagrar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="2480f-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2480f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2480f-120">-Name</span></span>
<span data-ttu-id="2480f-121">Anger namnet på den tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="2480f-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2480f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2480f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2480f-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2480f-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2480f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2480f-124">CommonParameters</span></span>
<span data-ttu-id="2480f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2480f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2480f-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2480f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2480f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2480f-127">INPUTS</span></span>

### <span data-ttu-id="2480f-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="2480f-128">None</span></span>
<span data-ttu-id="2480f-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2480f-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2480f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2480f-130">OUTPUTS</span></span>

## <span data-ttu-id="2480f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2480f-131">NOTES</span></span>

## <span data-ttu-id="2480f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2480f-132">RELATED LINKS</span></span>

