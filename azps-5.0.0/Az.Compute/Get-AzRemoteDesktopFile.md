---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272307"
---
# <span data-ttu-id="3b83e-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="3b83e-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="3b83e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b83e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b83e-103">Hämtar en. RDP-fil.</span><span class="sxs-lookup"><span data-stu-id="3b83e-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="3b83e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b83e-104">SYNTAX</span></span>

### <span data-ttu-id="3b83e-105">Bar</span><span class="sxs-lookup"><span data-stu-id="3b83e-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b83e-106">Start</span><span class="sxs-lookup"><span data-stu-id="3b83e-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b83e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b83e-107">DESCRIPTION</span></span>
<span data-ttu-id="3b83e-108">Cmdleten **Get-AzRemoteDesktopFile** hämtar en RDP-fil (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="3b83e-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="3b83e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b83e-109">EXAMPLES</span></span>

### <span data-ttu-id="3b83e-110">Exempel 1: Hämta en fjärr skrivbords fil</span><span class="sxs-lookup"><span data-stu-id="3b83e-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="3b83e-111">Det här kommandot får fjärr skrivbords filen för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3b83e-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="3b83e-112">Kommandot sparar resultatet i filen med namnet D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="3b83e-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="3b83e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b83e-113">PARAMETERS</span></span>

### <span data-ttu-id="3b83e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b83e-114">-DefaultProfile</span></span>
<span data-ttu-id="3b83e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b83e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b83e-116">-Lansera</span><span class="sxs-lookup"><span data-stu-id="3b83e-116">-Launch</span></span>
<span data-ttu-id="3b83e-117">Anger att denna cmdlet startar fjärr skrivbord när den får. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="3b83e-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b83e-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="3b83e-118">-LocalPath</span></span>
<span data-ttu-id="3b83e-119">Anger lokal fullständig sökväg där denna cmdlet lagrar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="3b83e-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b83e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b83e-120">-Name</span></span>
<span data-ttu-id="3b83e-121">Anger namnet på den tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="3b83e-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b83e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b83e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b83e-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3b83e-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b83e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b83e-124">CommonParameters</span></span>
<span data-ttu-id="3b83e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b83e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b83e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b83e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b83e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b83e-127">INPUTS</span></span>

### <span data-ttu-id="3b83e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3b83e-128">System.String</span></span>

## <span data-ttu-id="3b83e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b83e-129">OUTPUTS</span></span>

### <span data-ttu-id="3b83e-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="3b83e-130">System.Void</span></span>

## <span data-ttu-id="3b83e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b83e-131">NOTES</span></span>

## <span data-ttu-id="3b83e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b83e-132">RELATED LINKS</span></span>
