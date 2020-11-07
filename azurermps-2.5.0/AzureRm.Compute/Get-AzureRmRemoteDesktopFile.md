---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929505"
---
# <span data-ttu-id="37b10-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="37b10-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="37b10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37b10-102">SYNOPSIS</span></span>
<span data-ttu-id="37b10-103">Hämtar en. RDP-fil.</span><span class="sxs-lookup"><span data-stu-id="37b10-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37b10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37b10-104">SYNTAX</span></span>

### <span data-ttu-id="37b10-105">Bar</span><span class="sxs-lookup"><span data-stu-id="37b10-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37b10-106">Start</span><span class="sxs-lookup"><span data-stu-id="37b10-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b10-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37b10-107">DESCRIPTION</span></span>
<span data-ttu-id="37b10-108">Cmdleten **Get-AzureRmRemoteDesktopFile** hämtar en RDP-fil (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="37b10-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="37b10-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37b10-109">EXAMPLES</span></span>

### <span data-ttu-id="37b10-110">Exempel 1: Hämta en fjärr skrivbords fil</span><span class="sxs-lookup"><span data-stu-id="37b10-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="37b10-111">Det här kommandot får fjärr skrivbords filen för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="37b10-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="37b10-112">Kommandot sparar resultatet i filen med namnet D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="37b10-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="37b10-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37b10-113">PARAMETERS</span></span>

### <span data-ttu-id="37b10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b10-114">-DefaultProfile</span></span>
<span data-ttu-id="37b10-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37b10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b10-116">-Lansera</span><span class="sxs-lookup"><span data-stu-id="37b10-116">-Launch</span></span>
<span data-ttu-id="37b10-117">Anger att denna cmdlet startar fjärr skrivbord när den får. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="37b10-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="37b10-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="37b10-118">-LocalPath</span></span>
<span data-ttu-id="37b10-119">Anger lokal fullständig sökväg där denna cmdlet lagrar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="37b10-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="37b10-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="37b10-120">-Name</span></span>
<span data-ttu-id="37b10-121">Anger namnet på den tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="37b10-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="37b10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b10-122">-ResourceGroupName</span></span>
<span data-ttu-id="37b10-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="37b10-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="37b10-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b10-124">CommonParameters</span></span>
<span data-ttu-id="37b10-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b10-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b10-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b10-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b10-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37b10-127">INPUTS</span></span>

### <span data-ttu-id="37b10-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="37b10-128">None</span></span>
<span data-ttu-id="37b10-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="37b10-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37b10-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37b10-130">OUTPUTS</span></span>

## <span data-ttu-id="37b10-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37b10-131">NOTES</span></span>

## <span data-ttu-id="37b10-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37b10-132">RELATED LINKS</span></span>

