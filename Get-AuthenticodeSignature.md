
## Get-AuthenticodeSignature

```
PS C:\Users\test\Desktop> Get-Help -Parameter * Get-AuthenticodeSignature

-FilePath <String[]>
    Specifies the path to the file being examined. Wildcards are permitted, but they must lead to a single file. The parameter name ("FilePath") is optional.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByValue, ByPropertyName)
    Accept wildcard characters?  true


-LiteralPath <String[]>
    Specifies the path to the file being examined. Unlike FilePath, the value of the LiteralPath parameter is used exactly as it is typed. No characters are interpreted as wildcards. If the path includes escape characters, enclose it in single quotation marks. Single quotation marks tell Windows
    PowerShell not to interpret any characters as escape sequences.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


```

**-FilePath**

```
PS C:\Users\test\Desktop> Get-AuthenticodeSignature -FilePath C:\Windows\system32\*.exe | Where-Object {$_.SignerCertificate}


    Directory: C:\Windows\system32


SignerCertificate                         Status                                                                                                                           Path
-----------------                         ------                                                                                                                           ----
67B1757863E3EFF760EA9EBB02849AF07D3A8080  Valid                                                                                                                            aitstatic.exe
4F56A51B3BAE0667C16EC96A01778BD002D72494  Valid                                                                                                                            CompatTelRunner.exe
3384861E449A1542859DFBADB0C7D9A0B28110AA  Valid                                                                                                                            consent.exe
108E2BA23632620C427C570B6D9DB51AC31387FE  Valid                                                                                                                            icardagt.exe
018B222E21FBB2952304D04D1D87F736ED46DEA4  Valid                                                                                                                            MigAutoPlay.exe
3BDA323E552DB1FDE5F4FBEE75D6D5B2B187EEDC  Valid                                                                                                                            MpSigStub.exe
4F56A51B3BAE0667C16EC96A01778BD002D72494  Valid                                                                                                                            MRT.exe
4F56A51B3BAE0667C16EC96A01778BD002D72494  Valid                                                                                                                            ntkrnlpa.exe
4F56A51B3BAE0667C16EC96A01778BD002D72494  Valid                                                                                                                            ntoskrnl.exe
9617094A1CFB59AE7C1F7DFDB6739E4E7C40508F  Valid                                                                                                                            PresentationHost.exe
67B1757863E3EFF760EA9EBB02849AF07D3A8080  Valid                                                                                                                            TsWpfWrp.exe
9617094A1CFB59AE7C1F7DFDB6739E4E7C40508F  Valid                                                                                                                            vsjitdebugger.exe
E37814CFBE6DF35FC541E9B5CCD00C43E0096C88  Valid                                                                                                                            winload.exe
31448A571F750BCF76971CAADDD87498C6AF06CB  Valid                                                                                                                            winresume.exe


PS C:\Users\test\Desktop> Get-AuthenticodeSignature -FilePath C:\Windows\system32\*.exe | Where-Object { ! $_.SignerCertificate}


    Directory: C:\Windows\system32


SignerCertificate                         Status                                                                                                                           Path
-----------------                         ------                                                                                                                           ----
                                          NotSigned                                                                                                                        AdapterTroubleshooter.exe
                                          NotSigned                                                                                                                        aitagent.exe
                                          NotSigned                                                                                                                        alg.exe
                                          UnknownError                                                                                                                     append.exe
                                          NotSigned                                                                                                                        appidcertstorecheck.exe
                                          NotSigned                                                                                                                        appidpolicyconverter.exe
                                          NotSigned                                                                                                                        ARP.EXE
                                          NotSigned                                                                                                                        at.exe
                                          NotSigned                                                                                                                        AtBroker.exe
                                          NotSigned                                                                                                                        attrib.exe
                                          NotSigned                                                                                                                        audiodg.exe
                                          NotSigned                                                                                                                        auditpol.exe
                                          NotSigned                                                                                                                        autochk.exe
                                          NotSigned                                                                                                                        autoconv.exe
                                          NotSigned                                                                                                                        autofmt.exe
                                          NotSigned                                                                                                                        AxInstUI.exe
                                          NotSigned                                                                                                                        baaupdate.exe
                                          NotSigned                                                                                                                        bcdboot.exe
                                          NotSigned                                                                                                                        bcdedit.exe
                                          NotSigned                                                                                                                        BdeHdCfg.exe
                                          NotSigned                                                                                                                        BdeUISrv.exe
                                          NotSigned                                                                                                                        BdeUnlockWizard.exe
                                          NotSigned                                                                                                                        BitLockerWizard.exe
                                          NotSigned                                                                                                                        BitLockerWizardElev.exe
                                          NotSigned                                                                                                                        bitsadmin.exe
                                          NotSigned                                                                                                                        bootcfg.exe
                                          NotSigned                                                                                                                        bridgeunattend.exe
                                          NotSigned                                                                                                                        bthudtask.exe
                                          NotSigned                                                                                                                        cacls.exe
                                          NotSigned                                                                                                                        calc.exe
                                          NotSigned                                                                                                                        CertEnrollCtrl.exe
                                          NotSigned                                                                                                                        certreq.exe
                                          NotSigned                                                                                                                        certutil.exe
                                          NotSigned                                                                                                                        change.exe
                                          NotSigned                                                                                                                        charmap.exe
                                          NotSigned                                                                                                                        chglogon.exe
                                          NotSigned                                                                                                                        chgport.exe
                                          NotSigned                                                                                                                        chgusr.exe
                                          NotSigned                                                                                                                        chkdsk.exe
                                          NotSigned                                                                                                                        chkntfs.exe
                                          NotSigned                                                                                                                        choice.exe
                                          NotSigned                                                                                                                        cipher.exe
                                          NotSigned                                                                                                                        cleanmgr.exe
                                          NotSigned                                                                                                                        cliconfg.exe
                                          NotSigned                                                                                                                        clip.exe
                                          NotSigned                                                                                                                        cmd.exe
                                          NotSigned                                                                                                                        cmdkey.exe
                                          NotSigned                                                                                                                        cmdl32.exe
                                          NotSigned                                                                                                                        cmmon32.exe
                                          NotSigned                                                                                                                        cmstp.exe
                                          NotSigned                                                                                                                        cofire.exe
                                          NotSigned                                                                                                                        colorcpl.exe
                                          NotSigned                                                                                                                        comp.exe
                                          NotSigned                                                                                                                        compact.exe
                                          NotSigned                                                                                                                        CompMgmtLauncher.exe
                                          NotSigned                                                                                                                        ComputerDefaults.exe
                                          NotSigned                                                                                                                        conhost.exe
                                          NotSigned                                                                                                                        control.exe
                                          NotSigned                                                                                                                        convert.exe
                                          NotSigned                                                                                                                        credwiz.exe
                                          NotSigned                                                                                                                        cscript.exe
                                          NotSigned                                                                                                                        csrss.exe
                                          NotSigned                                                                                                                        csrstub.exe
                                          NotSigned                                                                                                                        ctfmon.exe
                                          NotSigned                                                                                                                        cttune.exe
                                          NotSigned                                                                                                                        cttunesvr.exe
                                          NotSigned                                                                                                                        dccw.exe
                                          NotSigned                                                                                                                        dcomcnfg.exe
                                          NotSigned                                                                                                                        ddodiag.exe
                                          UnknownError                                                                                                                     debug.exe
                                          NotSigned                                                                                                                        Defrag.exe
                                          NotSigned                                                                                                                        DeviceDisplayObjectProvider.exe
                                          NotSigned                                                                                                                        DeviceEject.exe
                                          NotSigned                                                                                                                        DevicePairingWizard.exe
                                          NotSigned                                                                                                                        DeviceProperties.exe
                                          NotSigned                                                                                                                        DFDWiz.exe
                                          NotSigned                                                                                                                        dfrgui.exe
                                          NotSigned                                                                                                                        dialer.exe
                                          NotSigned                                                                                                                        diantz.exe
                                          NotSigned                                                                                                                        dinotify.exe
                                          NotSigned                                                                                                                        diskpart.exe
                                          NotSigned                                                                                                                        diskperf.exe
                                          NotSigned                                                                                                                        diskraid.exe
                                          NotSigned                                                                                                                        Dism.exe
                                          NotSigned                                                                                                                        dispdiag.exe
                                          NotSigned                                                                                                                        DisplaySwitch.exe
                                          NotSigned                                                                                                                        djoin.exe
                                          NotSigned                                                                                                                        dllhost.exe
                                          NotSigned                                                                                                                        dllhst3g.exe
                                          NotSigned                                                                                                                        dnscacheugc.exe
                                          NotSigned                                                                                                                        doskey.exe
                                          UnknownError                                                                                                                     dosx.exe
                                          NotSigned                                                                                                                        dpapimig.exe
                                          NotSigned                                                                                                                        DpiScaling.exe
                                          NotSigned                                                                                                                        dplaysvr.exe
                                          NotSigned                                                                                                                        dpnsvr.exe
                                          NotSigned                                                                                                                        driverquery.exe
                                          NotSigned                                                                                                                        drvinst.exe
                                          UnknownError                                                                                                                     DRWATSON.EXE
                                          NotSigned                                                                                                                        dvdplay.exe
                                          NotSigned                                                                                                                        dvdupgrd.exe
                                          NotSigned                                                                                                                        dwm.exe
                                          NotSigned                                                                                                                        DWWIN.EXE
                                          NotSigned                                                                                                                        dxdiag.exe
                                          NotSigned                                                                                                                        Dxpserver.exe
                                          NotSigned                                                                                                                        Eap3Host.exe
                                          UnknownError                                                                                                                     edlin.exe
                                          NotSigned                                                                                                                        efsui.exe
                                          NotSigned                                                                                                                        EhStorAuthn.exe
                                          NotSigned                                                                                                                        esentutl.exe
                                          NotSigned                                                                                                                        eudcedit.exe
                                          NotSigned                                                                                                                        eventcreate.exe
                                          NotSigned                                                                                                                        eventvwr.exe
                                          UnknownError                                                                                                                     exe2bin.exe
                                          NotSigned                                                                                                                        expand.exe
                                          NotSigned                                                                                                                        extrac32.exe
                                          UnknownError                                                                                                                     fastopen.exe
                                          NotSigned                                                                                                                        fc.exe
                                          NotSigned                                                                                                                        find.exe
                                          NotSigned                                                                                                                        findstr.exe
                                          NotSigned                                                                                                                        finger.exe
                                          NotSigned                                                                                                                        fixmapi.exe
                                          NotSigned                                                                                                                        fltMC.exe
                                          NotSigned                                                                                                                        fontview.exe
                                          NotSigned                                                                                                                        forfiles.exe
                                          NotSigned                                                                                                                        fsquirt.exe
                                          NotSigned                                                                                                                        fsutil.exe
                                          NotSigned                                                                                                                        ftp.exe
                                          NotSigned                                                                                                                        fvenotify.exe
                                          NotSigned                                                                                                                        fveprompt.exe
                                          NotSigned                                                                                                                        FXSCOVER.exe
                                          NotSigned                                                                                                                        FXSSVC.exe
                                          NotSigned                                                                                                                        FXSUNATD.exe
                                          UnknownError                                                                                                                     GDI.EXE
                                          NotSigned                                                                                                                        getmac.exe
                                          NotSigned                                                                                                                        GettingStarted.exe
                                          NotSigned                                                                                                                        gpresult.exe
                                          NotSigned                                                                                                                        gpscript.exe
                                          NotSigned                                                                                                                        gpupdate.exe
                                          NotSigned                                                                                                                        grpconv.exe
                                          NotSigned                                                                                                                        hdwwiz.exe
                                          NotSigned                                                                                                                        help.exe
                                          NotSigned                                                                                                                        HOSTNAME.EXE
                                          NotSigned                                                                                                                        hwrcomp.exe
                                          NotSigned                                                                                                                        hwrreg.exe
                                          NotSigned                                                                                                                        icacls.exe
                                          NotSigned                                                                                                                        icsunattend.exe
                                          NotSigned                                                                                                                        ie4uinit.exe
                                          NotSigned                                                                                                                        ieetwcollector.exe
                                          NotSigned                                                                                                                        ieUnatt.exe
                                          NotSigned                                                                                                                        iexpress.exe
                                          NotSigned                                                                                                                        iisreset.exe
                                          NotSigned                                                                                                                        InfDefaultInstall.exe
                                          NotSigned                                                                                                                        ipconfig.exe
                                          NotSigned                                                                                                                        irftp.exe
                                          NotSigned                                                                                                                        iscsicli.exe
                                          NotSigned                                                                                                                        iscsicpl.exe
                                          NotSigned                                                                                                                        isoburn.exe
                                          NotSigned                                                                                                                        klist.exe
                                          UnknownError                                                                                                                     krnl386.exe
                                          NotSigned                                                                                                                        ksetup.exe
                                          NotSigned                                                                                                                        ktmutil.exe
                                          NotSigned                                                                                                                        label.exe
                                          NotSigned                                                                                                                        LocationNotifications.exe
                                          NotSigned                                                                                                                        Locator.exe
                                          NotSigned                                                                                                                        lodctr.exe
                                          NotSigned                                                                                                                        logagent.exe
                                          NotSigned                                                                                                                        logman.exe
                                          NotSigned                                                                                                                        logoff.exe
                                          NotSigned                                                                                                                        LogonUI.exe
                                          NotSigned                                                                                                                        lpksetup.exe
                                          NotSigned                                                                                                                        lpremove.exe
                                          NotSigned                                                                                                                        lsass.exe
                                          NotSigned                                                                                                                        lsm.exe
                                          NotSigned                                                                                                                        Magnify.exe
                                          NotSigned                                                                                                                        makecab.exe
                                          NotSigned                                                                                                                        manage-bde.exe
                                          NotSigned                                                                                                                        mblctr.exe
                                          NotSigned                                                                                                                        mcbuilder.exe
                                          NotSigned                                                                                                                        mctadmin.exe
                                          NotSigned                                                                                                                        MdRes.exe
                                          NotSigned                                                                                                                        MdSched.exe
                                          UnknownError                                                                                                                     mem.exe
                                          NotSigned                                                                                                                        mfpmp.exe
                                          NotSigned                                                                                                                        mmc.exe
                                          NotSigned                                                                                                                        mobsync.exe
                                          NotSigned                                                                                                                        mountvol.exe
                                          NotSigned                                                                                                                        mpnotify.exe
                                          NotSigned                                                                                                                        MRINFO.EXE
                                          UnknownError                                                                                                                     mscdexnt.exe
                                          NotSigned                                                                                                                        msconfig.exe
                                          NotSigned                                                                                                                        msdt.exe
                                          NotSigned                                                                                                                        msdtc.exe
                                          NotSigned                                                                                                                        msfeedssync.exe
                                          NotSigned                                                                                                                        msg.exe
                                          NotSigned                                                                                                                        mshta.exe
                                          NotSigned                                                                                                                        msiexec.exe
                                          NotSigned                                                                                                                        msinfo32.exe
                                          NotSigned                                                                                                                        mspaint.exe
                                          NotSigned                                                                                                                        msra.exe
                                          NotSigned                                                                                                                        MsSpellCheckingFacility.exe
                                          NotSigned                                                                                                                        mstsc.exe
                                          NotSigned                                                                                                                        mtstocom.exe
                                          NotSigned                                                                                                                        MuiUnattend.exe
                                          NotSigned                                                                                                                        MultiDigiMon.exe
                                          NotSigned                                                                                                                        NAPSTAT.EXE
                                          NotSigned                                                                                                                        Narrator.exe
                                          NotSigned                                                                                                                        nbtstat.exe
                                          NotSigned                                                                                                                        ncat.exe
                                          NotSigned                                                                                                                        ndadmin.exe
                                          NotSigned                                                                                                                        net.exe
                                          NotSigned                                                                                                                        net1.exe
                                          NotSigned                                                                                                                        netbtugc.exe
                                          NotSigned                                                                                                                        netcfg.exe
                                          NotSigned                                                                                                                        netiougc.exe
                                          NotSigned                                                                                                                        Netplwiz.exe
                                          NotSigned                                                                                                                        NetProj.exe
                                          NotSigned                                                                                                                        netsh.exe
                                          NotSigned                                                                                                                        NETSTAT.EXE
                                          NotSigned                                                                                                                        newdev.exe
                                          UnknownError                                                                                                                     nlsfunc.exe
                                          NotSigned                                                                                                                        nltest.exe
                                          NotSigned                                                                                                                        notepad.exe
                                          NotSigned                                                                                                                        nslookup.exe
                                          NotSigned                                                                                                                        ntprint.exe
                                          NotSigned                                                                                                                        ntvdm.exe
                                          NotSigned                                                                                                                        ocsetup.exe
                                          NotSigned                                                                                                                        odbcad32.exe
                                          NotSigned                                                                                                                        odbcconf.exe
                                          NotSigned                                                                                                                        openfiles.exe
                                          NotSigned                                                                                                                        OptionalFeatures.exe
                                          NotSigned                                                                                                                        osk.exe
                                          NotSigned                                                                                                                        OxpsConverter.exe
                                          NotSigned                                                                                                                        p2phost.exe
                                          NotSigned                                                                                                                        PATHPING.EXE
                                          NotSigned                                                                                                                        pcalua.exe
                                          NotSigned                                                                                                                        pcaui.exe
                                          NotSigned                                                                                                                        pcawrk.exe
                                          NotSigned                                                                                                                        pcwrun.exe
                                          NotSigned                                                                                                                        perfmon.exe
                                          NotSigned                                                                                                                        PING.EXE
                                          NotSigned                                                                                                                        PkgMgr.exe
                                          NotSigned                                                                                                                        plasrv.exe
                                          NotSigned                                                                                                                        PnPUnattend.exe
                                          NotSigned                                                                                                                        PnPutil.exe
                                          NotSigned                                                                                                                        poqexec.exe
                                          NotSigned                                                                                                                        powercfg.exe
                                          NotSigned                                                                                                                        PresentationSettings.exe
                                          NotSigned                                                                                                                        prevhost.exe
                                          NotSigned                                                                                                                        print.exe
                                          NotSigned                                                                                                                        PrintBrmUi.exe
                                          NotSigned                                                                                                                        printfilterpipelinesvc.exe
                                          NotSigned                                                                                                                        PrintIsolationHost.exe
                                          NotSigned                                                                                                                        printui.exe
                                          NotSigned                                                                                                                        proquota.exe
                                          NotSigned                                                                                                                        psr.exe
                                          NotSigned                                                                                                                        PushPrinterConnections.exe
                                          NotSigned                                                                                                                        qappsrv.exe
                                          NotSigned                                                                                                                        qprocess.exe
                                          NotSigned                                                                                                                        query.exe
                                          NotSigned                                                                                                                        quser.exe
                                          NotSigned                                                                                                                        qwinsta.exe
                                          NotSigned                                                                                                                        rasautou.exe
                                          NotSigned                                                                                                                        rasdial.exe
                                          NotSigned                                                                                                                        raserver.exe
                                          NotSigned                                                                                                                        rasphone.exe
                                          NotSigned                                                                                                                        rdpclip.exe
                                          NotSigned                                                                                                                        rdpinit.exe
                                          NotSigned                                                                                                                        rdpshell.exe
                                          NotSigned                                                                                                                        rdpsign.exe
                                          NotSigned                                                                                                                        rdrleakdiag.exe
                                          NotSigned                                                                                                                        rdrmemptylst.exe
                                          NotSigned                                                                                                                        RDVGHelper.exe
                                          NotSigned                                                                                                                        ReAgentc.exe
                                          NotSigned                                                                                                                        recdisc.exe
                                          NotSigned                                                                                                                        recover.exe
                                          UnknownError                                                                                                                     redir.exe
                                          NotSigned                                                                                                                        reg.exe
                                          NotSigned                                                                                                                        regedt32.exe
                                          NotSigned                                                                                                                        regini.exe
                                          NotSigned                                                                                                                        Register-CimProvider.exe
                                          NotSigned                                                                                                                        RegisterIEPKEYs.exe
                                          NotSigned                                                                                                                        regsvr32.exe
                                          NotSigned                                                                                                                        rekeywiz.exe
                                          NotSigned                                                                                                                        relog.exe
                                          NotSigned                                                                                                                        RelPost.exe
                                          NotSigned                                                                                                                        repair-bde.exe
                                          NotSigned                                                                                                                        replace.exe
                                          NotSigned                                                                                                                        reset.exe
                                          NotSigned                                                                                                                        resmon.exe
                                          NotSigned                                                                                                                        RMActivate.exe
                                          NotSigned                                                                                                                        RMActivate_isv.exe
                                          NotSigned                                                                                                                        RMActivate_ssp.exe
                                          NotSigned                                                                                                                        RMActivate_ssp_isv.exe
                                          NotSigned                                                                                                                        RmClient.exe
                                          NotSigned                                                                                                                        Robocopy.exe
                                          NotSigned                                                                                                                        ROUTE.EXE
                                          NotSigned                                                                                                                        RpcPing.exe
                                          NotSigned                                                                                                                        rrinstaller.exe
                                          NotSigned                                                                                                                        rstrui.exe
                                          NotSigned                                                                                                                        runas.exe
                                          NotSigned                                                                                                                        rundll32.exe
                                          NotSigned                                                                                                                        RunLegacyCPLElevated.exe
                                          NotSigned                                                                                                                        runonce.exe
                                          NotSigned                                                                                                                        rwinsta.exe
                                          NotSigned                                                                                                                        sbunattend.exe
                                          NotSigned                                                                                                                        sc.exe
                                          NotSigned                                                                                                                        schtasks.exe
                                          NotSigned                                                                                                                        sdbinst.exe
                                          NotSigned                                                                                                                        sdchange.exe
                                          NotSigned                                                                                                                        sdclt.exe
                                          NotSigned                                                                                                                        sdiagnhost.exe
                                          NotSigned                                                                                                                        SearchFilterHost.exe
                                          NotSigned                                                                                                                        SearchIndexer.exe
                                          NotSigned                                                                                                                        SearchProtocolHost.exe
                                          NotSigned                                                                                                                        SecEdit.exe
                                          NotSigned                                                                                                                        secinit.exe
                                          NotSigned                                                                                                                        services.exe
                                          NotSigned                                                                                                                        sethc.exe
                                          NotSigned                                                                                                                        SetIEInstalledDate.exe
                                          NotSigned                                                                                                                        setspn.exe
                                          NotSigned                                                                                                                        setupcl.exe
                                          NotSigned                                                                                                                        setupSNK.exe
                                          NotSigned                                                                                                                        setupugc.exe
                                          UnknownError                                                                                                                     setver.exe
                                          NotSigned                                                                                                                        setx.exe
                                          NotSigned                                                                                                                        sfc.exe
                                          NotSigned                                                                                                                        shadow.exe
                                          UnknownError                                                                                                                     share.exe
                                          NotSigned                                                                                                                        shrpubw.exe
                                          NotSigned                                                                                                                        shutdown.exe
                                          NotSigned                                                                                                                        sigverif.exe
                                          NotSigned                                                                                                                        slui.exe
                                          NotSigned                                                                                                                        smss.exe
                                          NotSigned                                                                                                                        SndVol.exe
                                          NotSigned                                                                                                                        SnippingTool.exe
                                          NotSigned                                                                                                                        snmptrap.exe
                                          NotSigned                                                                                                                        sort.exe
                                          NotSigned                                                                                                                        SoundRecorder.exe
                                          NotSigned                                                                                                                        spinstall.exe
                                          NotSigned                                                                                                                        spoolsv.exe
                                          NotSigned                                                                                                                        sppsvc.exe
                                          NotSigned                                                                                                                        spreview.exe
                                          NotSigned                                                                                                                        srdelayed.exe
                                          NotSigned                                                                                                                        StikyNot.exe
                                          NotSigned                                                                                                                        subst.exe
                                          NotSigned                                                                                                                        svchost.exe
                                          NotSigned                                                                                                                        sxstrace.exe
                                          NotSigned                                                                                                                        SyncHost.exe
                                          UnknownError                                                                                                                     sysedit.exe
                                          NotSigned                                                                                                                        syskey.exe
                                          NotSigned                                                                                                                        systeminfo.exe
                                          NotSigned                                                                                                                        SystemPropertiesAdvanced.exe
                                          NotSigned                                                                                                                        SystemPropertiesComputerName.exe
                                          NotSigned                                                                                                                        SystemPropertiesDataExecutionPrevention.exe
                                          NotSigned                                                                                                                        SystemPropertiesHardware.exe
                                          NotSigned                                                                                                                        SystemPropertiesPerformance.exe
                                          NotSigned                                                                                                                        SystemPropertiesProtection.exe
                                          NotSigned                                                                                                                        SystemPropertiesRemote.exe
                                          NotSigned                                                                                                                        systray.exe
                                          NotSigned                                                                                                                        tabcal.exe
                                          NotSigned                                                                                                                        takeown.exe
                                          NotSigned                                                                                                                        TapiUnattend.exe
                                          NotSigned                                                                                                                        taskeng.exe
                                          NotSigned                                                                                                                        taskhost.exe
                                          NotSigned                                                                                                                        taskkill.exe
                                          NotSigned                                                                                                                        tasklist.exe
                                          NotSigned                                                                                                                        taskmgr.exe
                                          NotSigned                                                                                                                        tcmsetup.exe
                                          NotSigned                                                                                                                        TCPSVCS.EXE
                                          NotSigned                                                                                                                        TFTP.EXE
                                          NotSigned                                                                                                                        timeout.exe
                                          NotSigned                                                                                                                        TpmInit.exe
                                          NotSigned                                                                                                                        tracerpt.exe
                                          NotSigned                                                                                                                        TRACERT.EXE
                                          NotSigned                                                                                                                        tscon.exe
                                          NotSigned                                                                                                                        tsdiscon.exe
                                          NotSigned                                                                                                                        tskill.exe
                                          NotSigned                                                                                                                        TSTheme.exe
                                          NotSigned                                                                                                                        TsUsbRedirectionGroupPolicyControl.exe
                                          NotSigned                                                                                                                        TSWbPrxy.exe
                                          NotSigned                                                                                                                        typeperf.exe
                                          NotSigned                                                                                                                        tzutil.exe
                                          NotSigned                                                                                                                        ucsvc.exe
                                          NotSigned                                                                                                                        UI0Detect.exe
                                          NotSigned                                                                                                                        unlodctr.exe
                                          NotSigned                                                                                                                        unregmp2.exe
                                          NotSigned                                                                                                                        upnpcont.exe
                                          UnknownError                                                                                                                     USER.EXE
                                          NotSigned                                                                                                                        UserAccountControlSettings.exe
                                          NotSigned                                                                                                                        userinit.exe
                                          NotSigned                                                                                                                        Utilman.exe
                                          NotSigned                                                                                                                        VaultCmd.exe
                                          NotSigned                                                                                                                        VaultSysUi.exe
                                          NotSigned                                                                                                                        vds.exe
                                          NotSigned                                                                                                                        vdsldr.exe
                                          NotSigned                                                                                                                        verclsid.exe
                                          NotSigned                                                                                                                        verifier.exe
                                          NotSigned                                                                                                                        vmicsvc.exe
                                          NotSigned                                                                                                                        vssadmin.exe
                                          NotSigned                                                                                                                        VSSVC.exe
                                          NotSigned                                                                                                                        w32tm.exe
                                          NotSigned                                                                                                                        waitfor.exe
                                          NotSigned                                                                                                                        wbadmin.exe
                                          NotSigned                                                                                                                        wbengine.exe
                                          NotSigned                                                                                                                        wecutil.exe
                                          NotSigned                                                                                                                        WerFault.exe
                                          NotSigned                                                                                                                        WerFaultSecure.exe
                                          NotSigned                                                                                                                        wermgr.exe
                                          NotSigned                                                                                                                        wevtutil.exe
                                          NotSigned                                                                                                                        wextract.exe
                                          NotSigned                                                                                                                        WFS.exe
                                          NotSigned                                                                                                                        where.exe
                                          NotSigned                                                                                                                        whoami.exe
                                          NotSigned                                                                                                                        wiaacmgr.exe
                                          NotSigned                                                                                                                        wimserv.exe
                                          NotSigned                                                                                                                        WindowsAnytimeUpgradeResults.exe
                                          NotSigned                                                                                                                        wininit.exe
                                          NotSigned                                                                                                                        winlogon.exe
                                          NotSigned                                                                                                                        winrs.exe
                                          NotSigned                                                                                                                        winrshost.exe
                                          NotSigned                                                                                                                        WinSAT.exe
                                          UnknownError                                                                                                                     WINSPOOL.EXE
                                          NotSigned                                                                                                                        winver.exe
                                          NotSigned                                                                                                                        wisptis.exe
                                          NotSigned                                                                                                                        wksprt.exe
                                          NotSigned                                                                                                                        wlanext.exe
                                          NotSigned                                                                                                                        wlrmdr.exe
                                          UnknownError                                                                                                                     WOWDEB.EXE
                                          UnknownError                                                                                                                     WOWEXEC.EXE
                                          NotSigned                                                                                                                        WPDShextAutoplay.exe
                                          NotSigned                                                                                                                        wpnpinst.exe
                                          NotSigned                                                                                                                        write.exe
                                          NotSigned                                                                                                                        wscript.exe
                                          NotSigned                                                                                                                        WSManHTTPConfig.exe
                                          NotSigned                                                                                                                        wsmprovhost.exe
                                          NotSigned                                                                                                                        wsqmcons.exe
                                          NotSigned                                                                                                                        wuapp.exe
                                          NotSigned                                                                                                                        wuauclt.exe
                                          NotSigned                                                                                                                        WUDFHost.exe
                                          NotSigned                                                                                                                        wusa.exe
                                          NotSigned                                                                                                                        xcopy.exe
                                          NotSigned                                                                                                                        xpsrchvw.exe
                                          NotSigned                                                                                                                        xwizard.exe


```
